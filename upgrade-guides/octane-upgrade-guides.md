# Octane Upgrade Guides

> This guide is currently a work in progress. If you'd like to help out, check out the [Contributing guide](../contributing.md) to get started!

This section of the Atlas is dedicated to helping you upgrade your applications and addons to Ember Octane, the first major edition of Ember!

### What belongs here?

The official Ember Guides have an Octane edition upgrade guide which covers the basic, but these guides are meant to cover the upgrade in more depth. We aim to have guides that:

* **Cover alternative upgrade paths.** For instance, the official Ember guides recommend using classic classes \(e.g. `EmberObject.extend()`\) until you can fully switch over to Glimmer components, but some users may want to adopt native classes earlier with classic components. The official guides are also aimed primarily at JavaScript users, and TypeScript could probably use some extra context and pointers. Ideally we should cover as many of these upgrade paths as we can, especially the most common ones.
* **Cover specific cases in depth.** During paradigm-shifting upgrades like Octane, there will be many different use cases that need to be converted. Specific combinations of observers, computed properties, and classic components will need to be converted to tracked properties and Glimmer components. In depth case-studies can help to clear up confusion here. As a rule of thumb - if a tricky conversation comes up on Discord or Stack Overflow about upgrading a specific case, and we _don't_ already have an example, we should add it here.





