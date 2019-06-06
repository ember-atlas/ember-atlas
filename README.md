# Ember Atlas Introduction

Hello, and welcome to the Ember Atlas, your one stop shop for navigating the world of Ember.js! This GitBook is a community driven project dedicated to documenting all things Ember and providing a place share knowledge. It is meant to work like a curated wiki, gathering as much information as possible, while simultaneously ensuring that information is easy to browse and has an overall consistent flow.

We don't have much content yet, but in time we hope to make the Atlas one of the first places Ember users look whenever they have a question about Ember. If you'd like to contribute, check out the contribution guide or ping us on Discord! We always welcome new guides and ideas 😄

## Where to Start?

The Atlas is meant to cover many different topics, aimed at many different kinds of developers! From first time Ember users and folks just checking out the framework to experienced veterans, we aim to cover any topic imaginable. Here are just a few places you could get started:

### Learning

If you're getting started:

* The [Official Ember Guides](https://guides.emberjs.com/release/) are the best place to start for first time Ember users who want to learn the basics.
* If you're coming from another ecosystem, like React or Vue, the [Coming From Another Ecosystem](learning/coming-from-another-ecosystem/) section is dedicated to guides that introduce Ember from that perspective.

For more advanced users, and further learning:

* The [Ember API Documentation](https://api.emberjs.com/)
* You can visit the [External Resources](learning/external-resources.md) page to find a bunch of external guides and resources that can use to learn more, including tutorials, courses, and blog posts!

### Upgrading

* If you're upgrading your app to Ember Octane, check out the [Ember Octane Upgrade Guides](upgrade-guides/octane-upgrade-guides.md).

## Why a "Wiki"?

You may be wondering why we need a community wiki. After all, Ember.js is a framework that is about conventions and zero-configuration, and the Ember guides are meant to be the canonical source-of-truth for those conventions. Doesn't having a community wiki run counter to that goal? Will it lead to more fragmentation in the ecosystem, and _more_ confusion instead of less? We don't believe it will, and here's why:

The Atlas and the official Ember Guides are meant to serve different purposes. The guides must:

1. Document the recommended, conventional, and beginner-friendly "happy path" for any given feature of Ember.
2. Maintain documentation for all previous versions of Ember.
3. Only document features that are part of the Ember framework itself, leaving out popular community addons and JavaScript libraries.
4. Ship documentation that is thoroughly reviewed, triple checked, high quality, and battle-tested.

This sets a very high bar for the content that becomes part of the guides, and can be a daunting task to new contributors. It also prevents us from documenting many different intermediate and advanced user stories, which often involve various community addons or techniques.

We won't be able to cover every topic under the sun, but we can try to capture and organize as much community knowledge as possible, especially around common use cases and combinations. We can take the output of the many Discord conversations, Discourse posts, and Stack Overflow answers and put them in one place. We can help pick up the burden that popular addons have, making their tools easy to learn and approach and use with

To that end, the Atlas has some explicit goals and non-goals.

### Goals

* **Fill in the gaps.** We should document the most common "paths" that Ember developers tread which _aren't_ documented elsewhere.
* **Provide or link to an answer for every question.** Developers should be able to turn to the Atlas if they are completely lost, and learn at least a little bit more about what they are trying to do.
* **Be accepting of incomplete or in-progress docs.** Writing documentation is hard, and sometimes it takes multiple drafts from multiple authors to really nail down a particular topic. Incomplete docs can still be helpful, and can also serve as a starting point for future contributors, so we should work within those constraints.
* **Provide a place for experimentation.** The Atlas should be a place for new ideas for documentation and guides to grow, and in time possibly upstreamed if they are successful.
* **Strive for accurate content.** It's not helpful to anyone if documentation is out of date, incomplete, or flat-out wrong. At the same time, it's difficult to gather a lot of content from many contributors _and_ guarantee that everything is always accurate. The Atlas should be as open-by-default to new contributions as possible, and also open to revisions, corrections and updates over time.
* **Gather in-depth technical knowledge about Ember.js.** The main guides are great for beginner and intermediate users, but there isn't much content for _advanced_ users, and much of what is out there is scattered through random blog posts, gists, and youtube videos. Centralizing this information will help spread knowledge and level of users and contributors.
* **Maintain** _**enough**_ **organization and curation.** It's easy for the signal to get lost in the noise, and that's a big part of the reason the Atlas exists in the first place! However, we also don't want to waste time bike shedding over where something should go. We should always make sure that developers can find the content they're looking for on the Atlas, and regularly review, revise, and edit the content in the wiki, while having an open mindset toward new contributions.

### Non-Goals

* **Duplicating content that is available elsewhere.** If a particular topic is already thoroughly documented in the Ember.js guides, or in an addons guides, or in a very thorough \(and up to date\) blog post, we should link to it instead.
* **Versioning content.** Maintaining multiple versions of content can be a major overhead, and given the breadth the Atlas aims to cover it's not feasible for us to version each guide as well. Some content will be versioned by its nature - for instance, upgrade guides - but anything else should focus on the current state of the world exclusively.
* **Documenting** _**everything**_. The Atlas strives to cast a wider net, but it's not possible to document every bespoke combination of addons, libraries, Ember versions, and build tools that exist in the wild. We'll try our best, but we should also know our limits.

