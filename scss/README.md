# SCSS Style Guide

We use [Sass](http://sass-lang.com) as our preprocessor of choice, because it allows us to conveniently structure our styles and avoid code duplication. We use the latest version of [LibSass](http://libsass.org) a blazing-fast C implementation of the Sass compiler. LibSass is nearly at feature parity with the original Ruby compiler, but it's still worth [checking compatibility](http://sass-compatibility.github.io) if something doesn't seem to be working correctly.

We use [Autoprefixer](https://github.com/postcss/autoprefixer) as a postprocessing step to add all of our vendor prefixes.

### Formatting

 * We use two-space indents (not tabs), and wrap line-width to approximately 80 characters for readability.
 * We write each property on a new line.
 * Use single-quotes for strings.
 * When dealing with lengths, a `0` value should never have a unit.

 ```scss
  // Yep
  .foo, .foo-bar,
  .baz {
    display: block;
    overflow: hidden;
    margin: 0 auto;
  }

  // Nope
  .foo,
  .foo-bar, .baz {
    display:block;
    overflow:hidden;
    margin:0px auto 0px }

 ```

### Good Code

 * Avoid using [magic numbers](http://en.wikipedia.org/wiki/Magic_number_(programming)#Unnamed_numerical_constants) if at all possible. Whenever possible, use base measurement units, like `$base-spacing`, to keep standard spacing throughout the site.
 * Always use color, font, and weight variables from Neue's `[variables.scss](https://github.com/DoSomething/neue/blob/dev/scss/_utilities/_variables.scss)` rather than hard-coding values. If you need to use a new value, consider adding it as a variable at the top of the block or file.
 * Use shorthands whenever possible, such as `margin: 0 auto` over `margin: 0 auto 0`.
 * Avoid nesting, aside from when writing pseudo-selectors or state classes. Otherwise, you can unintentionally output extremely specific selectors [which is a re-usability no-no](http://www.sitepoint.com/beware-selector-nesting-sass/).


### Architecture

We use a modified [BEM](https://css-tricks.com/bem-101/) naming scheme for our CSS classes.

 * Use __blocks__ for top-level components. Class names should be lower-case and hyphenated, e.g. `.block-item`.
 * Use __elements__ for child components inside a block. Elements are named with a double-underscore, e.g. `.block-item__element`.
 * Use __modifiers__ for variations on a block. __Modifiers are named with a compound selector and a class prefixed by a single dash.__ For example, `.block-item.-modifier`.

Each file should contain exactly _one_ block, except when creating [theme files](#). The file should be named the same as the block that is styled within it. For example, `.button { ... }` exists within `button.scss`.


### Patterns

 * Include [KSS](http://warpspire.com/kss/) comments for any patterns.


