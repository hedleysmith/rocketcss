Rocket CSS
----------

[Rocket CSS](https://github.com/hedleysmith/rocketcss) is a decoupled library of CSS components written using Sass.

Components are provided with some styling and configuration options but are designed to be used as a starting point in a custom design system.

Rocket also encourages the use of components from other libraries.

### Customising Components

It's up to you how you customise the components. Here are two suggested approaches

1) __Use Rocket components as a starting point.__ Go in and edit the component code directly, useful for larger projects where you're likely to deviate significantly from the original component and you want to have more control. A disadvantage of this is that if there are updates released for a component it'll be more difficult to take advantages of these.

2) __Configure and extend components.__ By keeping the original Rocket component you'll be able to take advantage of any updates that are released. Each component has a number of default configuration options documented at the start of the component file, these can be overridden elsewhere in the codebase. You could add your own customisations to a _theme.scss file which should be included before the component.

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
