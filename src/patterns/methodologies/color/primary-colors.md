---
title: Primary Colors
styles: base/variables.scss
maturity: ready
control: exclude
colors: 
  - name: $white
    hex: '#ffffff'
  - name: $grey
    hex: '#707070'
  - name: $green
    hex: '#8ea260'
  - name: $brown
    hex: '#7f6042';
  - name: $background
    hex: '#eeece8';
  - name: cardBackground
    hex: '#d8d4cc'
---
<style>
.set {
  display: flex;
  flex-wrap: wrap;
  margin: 0 -1rem;
  margin-top: 0;
  padding: 0;
  list-style: none;
}
li {
  flex: 1 0 20%;
  margin: 1rem;
}
.color {
  width: 100%;
  min-width: 160px;
  height: 80px;
  color: white;
  border: 1px solid whitesmoke;
  margin-bottom: 1rem;
}
p {
  margin: 0;
}
</style>
<ul class="set">
{% for item in page.colors %} 
  <li>
    <div class="color" style="background:{{ item.hex }}"></div> 
    <p>{{ item.name }}</p>
    {% if item.hex %}<p>{{ item.hex }}</p>{% endif %}
  </li>
{% endfor %}
</ul>