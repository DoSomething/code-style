# SCSS Style Guide

We use [Sass](http://sass-lang.com) as our preprocessor of choice, because it allows us to build maintainable code quickly. We use the the latest version of [LibSass](http://libsass.org), a blazing-fast C implementation of the Sass compiler, on most projects.

We use [Susy](http://susy.oddbird.net) to build our interfaces on a fluid grid. This helps ensure consistent measurements and provides rules for layouts to comfortably expand and contract in a multi-device world. Our standard grid is split up into sixteen columns, with a 24 pixel static gutter between columns.

We use [Autoprefixer](https://github.com/postcss/autoprefixer) as a postprocessing step to add all of our vendor prefixes. Vendor prefixes are added for the last 4 versions of evergreen browsers and the latest [Firefox ESR](https://www.mozilla.org/en-US/firefox/organizations/faq/) release.

### Formatting

 * Use two-space indents (not tabs), and wrap line-width to approximately 80 characters for readability.
 * Write each property on a new line.
 * Use single-quotes for strings.
 * When dealing with lengths, a zero value should never have a unit.

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
 * Always use color, font, and weight variables from Neue's [`variables.scss`](https://github.com/DoSomething/neue/blob/dev/scss/_utilities/_variables.scss) rather than hard-coding values. If you need to use a new value, consider adding it as a variable at the top of the block or file.
 * Use shorthands whenever possible, such as `margin: 0 auto` over `margin: 0 auto 0`.
 * Avoid nesting, aside from when writing pseudo-selectors or state classes. Otherwise, you can unintentionally output extremely specific selectors [which is a re-usability no-no](http://www.sitepoint.com/beware-selector-nesting-sass/).


### Architecture

We use a modified [BEM](https://css-tricks.com/bem-101/) naming scheme for our CSS classes.

 * __Blocks__ are top-level components. Class names should be lower-case and hyphenated, e.g. `.block-item`.
 * __Elements__ are child components inside a block. They are prefixed by the parent block and a double-underscore, e.g. `.block-item__element`.
 * __Modifiers__ are variations on a block. _Unlike classic BEM, we declare modifiers with a compound selector and a class prefixed by a single dash._ For example, `.block-item.-modifier`.

```scss
// An example block.
.block-item {
  background-color: $gray;

  &.-primary {
    background-color: $blue;
  }
}

// An element within block.
.block-item__doodad {
  // ...
}
```

Each file should contain exactly _one_ block, except when creating [theme files](#). The file should be named the same as the block that is styled within it. For example, `.button { ... }` exists within `button.scss`.


### Patterns

We build our interfaces using re-usable components, or _patterns_. This helps us keep things consistent through a growing codebase & iterate more rapidly by not re-inventing the wheel.

 * Include [KSS](http://warpspire.com/kss/) documentation for any patterns.
 * A pattern should only have modifiers at the block level. Avoid using individual modifiers for child elements if at all possible. This is probably an indication that a block should be split into two separate patterns.



