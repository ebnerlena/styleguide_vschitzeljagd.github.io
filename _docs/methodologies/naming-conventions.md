---
title: Naming Conventions
info: What name should you choose?
---

## BEM Naming Convention
In our CSS we try to stick to the BEM naming conventions by using block__element--modifier syntax for classes.
The classes are useful as than all elements are in the same hierachy and specificity.   
Also it helps create clear, strict relationships between CSS and HTML.  
  
BEM naming convention is the basis for an “Object Oriented CSS” (OOCSS) approach for writing CSS that encourages you to think about your stylesheets as a collection of “objects”: reusable, repeatable snippets that can be used independently throughout a website. (cite: <a href="https://github.com/airbnb/css">https://github.com/airbnb/css</a> ) 

Visit the official BEM documentation <a href="https://en.bem.info/methodology/">https://en.bem.info/methodology/</a>  
Find out more about OOCSS here <a href="https://github.com/stubbornella/oocss/wiki/">https://github.com/stubbornella/oocss/wiki</a>
  

## Example

```
// Example button component
.btn {
  position: relative;
  display: inline-block;
  vertical-align: middle;
  margin: 2%;
  padding: $small-pad $large-pad;
  background: $accentColor;
  border: none;
  border-radius: 12px;
  white-space: none;
  cursor: pointer;
  color: $white;
  line-height: 1;
  text-align: center;
  text-decoration: none;
  min-width: 100px;
  transition: all .3s ease-in;
  outline: none;
  -webkit-appearance: none;
  -moz-appearance: none;

  &:hover:not(.btn--active),
  &:focus {
    transform: scale(1.05);
    box-shadow: 0 0 8px rgba(0,0,0,0.3);
  }
}

.btn--active, .btn:active {
  color: transparent;
  transform: scale(0.98);
  box-shadow: 0 0 10px rgba(0,0,0,0.3);
}

.btn--disabled, .btn:disabled {
  pointer-events: none;
  background: $backgroundColor2;
}

.btn__icon {
  min-width: 0;
}
```

{% include pattern_block.html url='/src/patterns/components/button/default_button.html' %}

{% include pattern_block.html url='/src/patterns/components/button/disabled_button.html' %}
