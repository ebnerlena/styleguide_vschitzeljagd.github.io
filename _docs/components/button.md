---
title: Button
info: Use buttons to signal actions.
---

Buttons are used to signal actions e.g. create a new game task.  
Normally buttons contain text, but also at some places an white icon inside might be wanted.
In HTML we can use the button or link tag, although any other tag can be used, when giving him the .btn class.
  

{% include pattern_block.html url='/src/patterns/components/button/default_button.html' %}
A normal, clickable button gets bigger when you hover it.

{% include pattern_block.html url='/src/patterns/components/button/active_button.html' %}
An active button does not display the text anymore and pointer events will not occur any longer.

{% include pattern_block.html url='/src/patterns/components/button/disabled_button.html' %}
A button can be disabled, pointer events will not occur. No interaction is possible.

{% include pattern_block.html url='/src/patterns/components/button/icon_button.html' %}
A button can also include an image/icon instead of text.

