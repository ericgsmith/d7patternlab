# Drupal7 Pattern Lab Starter
This is a starter for using Pattern Lab with a Drupal 7 project. The Pattern Lab examples and data have been stripped 
down to the absolute basics, with some Drupal specific elements added.

This also aims to be a base to improve documentation for Drupal 7 front end projects.

## About Pattern     Lab
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

###Example
Uses a handful of core module stylesheets and the Bartik theme.

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
Each form item can have it's label, error state, required state and description altered in the global data.json file, or 
per template.

###Example
Shows the example data for a text area used in a pattern. This currently limits the page / pattern to use the same data 
for each field type. If this proves problematic we need to refactor the way this is controlled (the other option is hard
coding the classes / markup or adding new atoms for each field).

```
    "textarea" : {
        "description" : false,
        "required": false,
        "error": false,
        "label": "Text area"
    },
```

## Image styles
Add a new image atom for each image style created in Drupal.

## View modes
Currently we provide an example organism for the node teaser view mode. All available view modes should be documented / 
added to Pattern Lab.

## Colours and fonts
Colours and fonts are generated from their respective json file in the atom folder. Colours and font stacks can be added
to the json file and the markup will not need to be updated.
