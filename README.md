Rocket CSS
----------

#### [Rocket CSS](https://github.com/hedleysmith/rocketcss) is a collection of organised but independent frontend components.

__Rocket CSS__ gives you a solid and highly customisable starting point and is designed to built on top of to scale. You can also use components entirely independently.

## Features

* __Independent Components__ with explicitly declared dependencies
* __A Solid Starting Point__ much like other frontend frameworks Rocker CSS has a wide set of useful building blocks to build out a project quickly and easily
* __Interoperable__ Pick and choose from Rocket CSS, and use components and styling from other frameworks
* __Maintainable and Scalable__ files organised using Component Driven Design principles there is a clear path to build your own components and add styling for sections of your project
* __Plays well with React.js__ while Rocket CSS currently focuses on styling, it's simple to slot in JavaScript powered components and even state management

Rocket is not a plug-and-play prototyping kit. It's designed to give you a boost toward a more sustainable front end architecture.

## Getting Started

__Component folders explained__

* __Utility__ - Utility components will generally contain mixins used by other components, and declarative hooks used on the site (e.g .l-container, .grid-m). In other frameworks these types of components are known as 'helpers', 'abstractions', 'mixins' or 'functions'.
* __Base__ - these can be thought of as the first 'layer' of components that will be applied site-wide and used throughout the codebase, things like reset / normalize files, typography & colour configuration and global styling for HTML elements will go here.
* __Components__ - user interface components, things that users interact with and that are re-usable and implemented in many places on a site

### Using Components Stand-alone

Each component can be used independently fairly easily, if you'd like to do this go ahead and grab the Sass partial, look at any declared dependencies and be sure to include these dependencies as well.

### Using Rocket as a Framework

Starting a new project using all Rocket components will be similar to the way you start with many other front end frameworks (e.g Bootstrap, Foundation).

There are two alternative installation methods:

1. __Use Rocket as a starter-kit.__ This is the recommended method. Simply download Rocket, add a style.scss base partial and ```@import "rocket";```. From here you can add more folders and components to suit your needs. We recommend adding a 'spaces' folder and grouping related one-off components in separate sub-folders (e.g 'global', 'homepage', 'blog', 'user-profile'), adding UI components to the existing 'components' folder, base components to the existing 'base' folder and building up utility components in the existing 'utility' folder.

2. __Keep Rocket separate.__ To retain all of Rocket's

### Customising Components

Once you've started using Rocket you might want to customise some of the components, it's up to you how you do this. Here are two suggested approaches

1) __Use Rocket components as a starting point and edit.__ Go in and edit the component code directly, useful for larger projects where you're likely to deviate significantly from the original component and you want to have more control. A disadvantage of this is that if there are updates released for a component it'll be more difficult to take advantages of these.

2) __Configure and extend components.__ By keeping the original Rocket component you'll be able to take advantage of any updates that are released. Each component has a number of default configuration options documented at the start of the component file, these can be overridden elsewhere in the codebase. You could add your own customisations to a `_theme.scss` file which should be included before the component.

## Importing Components

With numerous front end component libraries out there it makes sense to harness them. Rocket provides a way to use and customise individual components from other libraries without having to follow their design patterns entirely.

### Foundation

__Installation__

1. Copy _functions.scss and _global.scss across.
2. Copy over the .scss file for the component you're installing.
3. Now attempt to compile the codebase, if there are any missing dependencies, figure out how to resolve them (this part can get a bit tricky).

__Javascript Components__

1. Foundation [requires Modernizr & jQuery > 2.1.0](http://foundation.zurb.com/docs/javascript.html) so include these as well as foundation.js - also, initialise foundation.

```
<script src="//cdnjs.cloudflare.com/ajax/libs/modernizr/2.8.3/modernizr.min.js"></script>
<script src="//code.jquery.com/jquery-2.1.4.min.js"></script>
<script src="/js/foundation.js"></script>
<script>
  $(document).foundation();
</script>
```

2. Copy the relevant .js file, e.g /js/foundation.tab.js

### Bootstrap

@todo

### Material Design Light

@todo

### Other Libraries

* [ExpandJS](http://expandjs.com/)
* [Ionic](http://ionicframework.com/docs/components)
* [UI Kit](https://github.com/uikit/uikit)

### Development

1. To test compilation, run ```sass _rocket.scss dist/rocket.css```
