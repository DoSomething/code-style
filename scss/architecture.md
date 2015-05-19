# SASS Architecture guidelines

This document outlines how to implent SASS architecture for the DoSomething applicationa and Neue pattern library.

### DoSomething App

All styles for the DoSomething site live in `lib/themes/dosometing/paraneue_dosometing/scss`. When adding new styling to the DoSomething site, add a new  `.scss` partial to one of subdirectories and then add the new partial in `app.scss` so that the new partial is included  in the build.

**SASS Architecture Outline**

- SCSS/
  - [content](#content)
  - helpers/
  - [overrides/](#overrides)
  - [patterns/](#patterns)
  - app.scss

**<a name="content"></a> Content**

The content directory holds partials for each "feature" on the DoSomething site. A feature refers to a specific section of the site, like campaigns or the auth flow. In many cases, these will be the node type of the page you're looking to theme. Each new "feature" should have it's own partial in this directory. The name of the partial should be easily correlated with the name of the new feature.

**<a name="overrides"></a> Overrides**

The overrides directory contains the `_drupal.scss` partial. If you need to override any default drupal styles, they should go in this file.

**<a name="patterns"></a> Patterns**

The patterns directory holds partials for patterns that are specific to the DoSomething site, but have the potential/should eventually be added to Neue. When working on a new feature, consider if a piece of the design could have multiple uses outside of that feature. If so, add a partial for that pattern to this directory. The name of the partial should be the name of the new pattern.

Patterns in this directory should be moved to Neue if used multiple times throughout the site. When adding the partial to `app.scss` make sure to add a `@TODO` to move to neue.
