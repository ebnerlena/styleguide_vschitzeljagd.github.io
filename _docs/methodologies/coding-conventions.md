---
title: Coding Conventions
info: What we use to keep our code clean.
---
## Pre Processors
We are using Sass CSS preprocessor to convert SCSS into CSS.

See the documentation here: <a href="https://sass-lang.com/"> https://sass-lang.com/ </a>

An typical SCSS Syntax example with identications and mixins for DRY would be as following:

```
// Variable declaration in scss/_abstracts/_variables
$white: #ffffff;

// Mixins in scss/_abstracts/
@mixin mobile {
    @media (max-width: 450px) {
      @content;
    }
}

// Navigation in scss/_components/
.nav {
    background-color: $primaryColor;
    color: $white;
    height: 70px;
    display: flex;
    z-index: 5;
    position: fixed;
    padding: 0 20px;

    @include mobile {
        padding-left: ($default_padding)/2;
        height: 65px;
    }

    .nav__header {
        list-style: none;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        padding: 0;
        margin: 0;
        width: 100vw;
    }
}
```

## 7-1 Pattern
We use a 7-1 architecture as recommended by the Sass Guidelines and import all files into the main.scss.
Another reason we use this pattern is, that it is very clearly structured. So you are able to find the file you are looking for quickly.

Find the description here <a href="https://sass-guidelin.es/de/">https://sass-guidelin.es/de/ </a>

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
We use REM as default unit. We do so to make sure that we always refer to the root element.

## CSS Normalize
Furthermore we use CSS Normalize to provide cross browser consistency in the default styling of HTMl elements.

Normalize `[_normalize.scss]` was extracted from [Normalize.css](https://github.com/necolas/normalize.css), copyright Nicolas Gallagher and Jonathan Neal.

## Spacings
We also use default margins, paddings and border-radius for our components. We user this to make sure, that there is equal spacing everywhere.  
  
They are defined as the following:
 
- $default_margin: 1rem;
- $default_padding: 1rem;
- $borderradius: 12px;

## Breakpoints

As our goal is to provide a responsive design we use the following breakpoints defined as mixins:

```
// mixins in scss/_abstract/mixins.scss

  @mixin desktop {
    @media (min-width: 1100px) {
      @content;
    }
  }

  @mixin tablet {
    @media (min-width: 450px) and (max-width: 1100px){
      @content;
    }
  }
  
  @mixin mobile {
    @media (max-width: 450px) {
      @content;
    }
  }
  
  @mixin maxwidthcontainer {
    max-width: 35rem;
  }
```
