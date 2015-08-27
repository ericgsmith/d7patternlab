# Drupal7 Pattern Lab Starter
This is a start for using Pattern Lab with a Drupal 7 project. The Patter Lab examples / starter patterns and data
have been stripped down to the absolute basics, with some Drupal specific elements added. This is less example based
that the standard Pattern Lab, and is intended to be used as a starter for D7.

This also aims to be a base to improve documentation for Drupal 7 front end projects.

This is completely un tested in the real world and I'm am keen to get feedback / testing / improvements under way. Please
use the GitHub issue queue for any issues / improvements.

## About Pattern Lab
- [Pattern Lab Website](http://patternlab.io/)
- [About Pattern Lab](http://patternlab.io/about.html)
- [Documentation](http://patternlab.io/docs/index.html)
- [Demo](http://demo.patternlab.io/)

## Importing Drupal Styles
New variables have been added to the data.json file to support importing styles from Drupal. The use case is if the 
developer does not want to start from a complete reset, and may want some core or base theme styles included in the 
pattern lab.

Use `drupalRoot` to point Pattern Lab at a Drupal installation to get CSS files from.
Use `drupalStyleSheets` to list any style sheets to import from Drupal (relative to the document root).

Example

```
    "drupalRoot" : "http://d7lab.local",
    "drupalStyleSheets" : [
        "/modules/system/system.base.css",
        "/modules/system/system.menus.css",
        "/modules/system/system.messages.css",
        "/modules/system/system.theme.css",
        "/modules/comment/comment.css",
        "/modules/field/theme/field.css",
        "/modules/node/node.css",
        "/modules/search/search.css",
        "/modules/user/user.css"
    ],
```

## Forms
Forms... forms... forms. These can be a cunt the theme in Drupal, so we have matched Drupals form classes to our form
atoms.

Each form item can have its label, error state, required state and description altered in data.json, or per template.

Example

```
    "textarea" : {
        "description" : false,
        "required": false,
        "error": false,
        "showLabel": true
    },
```

## Image styles
Please, please, please add a new image atom for each image style we create in Drupal.

## View modes
Drupal view modes are awesome. Currently we provide an example molecule for the teaser view modes. Again, please please
document all view modes.