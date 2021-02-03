---
title: Coding Conventions
info: What we use to keep our code clean.
---
## Pre Processors
We are using Sass CSS preprocessor to convert SCSS into CSS.

<a href="https://sass-lang.com/"> Have a look here </a>

scss example with identierung und nesting und mixins

## 7-1 Pattern
We use a 7-1 architecture as recommended by the Sass Guidelines and import all files into the main.scss.

link missing

- sass/
    - _abstracts/
        - _variables.scss    
        - _mixins.scss   

    - vendors/

    - base/
        - _normalize.scss        
        - _typography.scss 

    - layout/
        - _navigation.scss   
        - _grid.scss         
        - _header.scss       
        - _footer.scss       
        - _sidebar.scss      
        - _forms.scss        

    - components/
        - _buttons.scss      
        - _cards.scss     
        - _input.scss            

    - pages/
        - _home.scss    
        - _contact.scss      

    - themes/
        - _theme.scss   
        - _admin.scss     

    - main.scss 

## Units
We use REM as default unit so that we always refer to the root element.

## CSS Normalize
We use CSS Normalize to provide cross browser consistency in the feault styling of HTMl elements.

Normalize `[_normalize.scss]` was extracted from [Normalize.css](https://github.com/necolas/normalize.css), copyright Nicolas Gallagher and Jonathan Neal.

## Spacings
We try to use default margins, paddings and border-radius for our components defined as .
 
 - $default-margin:
 - $default-padding:
 - $default-borderradius:


