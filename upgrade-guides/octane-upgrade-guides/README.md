# Octane Upgrade Guide

> This guide is currently a work in progress. If you'd like to help out, check out the [Contributing guide](../../contributing.md) to get started!

This section of the Atlas is dedicated to helping you upgrade your applications and addons to Ember Octane, the first major edition of Ember! If you're lost and don't know where to start, this is the place for you.

## Getting Started

Upgrading your application can be a daunting task. Octane introduces a new programming model - new classes, new components, new property tracking, new template syntax, and more. The important thing to remember is that Ember supports both the Classic programming model \(the pre-Octane model\) and the Octane programming model at once. This means that you can convert your application one class or file at a time, progressively making progress as you also continue to ship features and build your application!

The general flow we recommend for tackling this upgrade is:

1. Run the codemods to convert template syntax and class syntax, and to add the **`@classic`** decorator to your classes.
2. Use the **`@classic`** decorator to track your progress, tackling, converting, and removing it from one class at a time.

## Running the Codemods

There are several codemods that'll help you get started with the transition to Octane:

* The [Native Class Codemod](https://github.com/ember-codemods/ember-native-class-codemod)
* The [Angle Bracket Codemod](https://github.com/rajasegar/ember-angle-brackets-codemod) \(Still a WIP\)
* The `this` conversion codemod \(Not ready yet\)

Run through each of these on the code that you are planning to convert, using their documentation to guide you through running the codemod.

## The @classic Decorator

The [classic decorator](https://github.com/pzuraq/ember-classic-decorator) is a class decorator designed to help you with this upgrade. When a class is decorated with the decorator, it means that there is still something in that class that needs to be converted to Octane's conventions. 

```javascript
@classic
export default class MyService extends Service {
  // `init` needs to be converted to `constructor`
  init() {
    // ...  
  }
  
  // This computed needs to be replaced with tracked properties
  @computed('some', 'props')
  get someComputed() {
    // ...
  }
  
  incrementCount() {
    // This method is a classic method, and needs to be rewritten
    // to something like `this.count++` (after converting count to @tracked) 
    this.incrementProperty('count');
  }
} 
```

The decorator is added automatically by the [native class codemod](https://github.com/ember-codemods/ember-native-class-codemod), and is removed entirely from production builds. It will throw linting errors and assertions if you are using classic APIs in classes that don't use the decorator, so it prevents you from accidentally removing it before a class has been converted.

## Updating Classes

After you've run the codemods and have the `@classic` decorator workflow setup, you can begin updating individual classes. There are three categories of classes you'll update:

* **Framework Classes,** like Routes/Controllers/Services/Helpers. You will need to remove all classic API usage from these classes, such as tracked properties and `this.get`/`this.set` before you can remove the `@classic` decorator.
* **Utility Classes,** which are any other classes that extend from `EmberObject`. These will need to be rewritten so they no longer extend from `EmberObject` before you can remove the `@classic` decorator.
* **Components,** which will need to be updated to Glimmer components before you can remove the `@classic` decorator.

In all three of these classes, you will have to remove classic APIs is order to fully remove the `@classic` decorator as well. Classic APIs include:

* Computed properties and observers \(replaced with tracked properties\)
* Lifecycle hooks like `init` and `destroy`
* Methods like `this.get` and `this.set`

In Framework classes, these are the _only_ things you need to convert, making them relatively simple, so we start you off there. 

