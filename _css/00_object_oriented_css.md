
### Object Oriented CSS 

You can have multiple `class` selectors. See below example of _object oriented_ css  styling:
```html
<div class="blue box"> blue box </div>
```
With the following css stylesheet:
```css
.blue {color:blue;}
.box {border: 5px solid black; background:lightblue; width:80px}
```
Will produce:
<h5 style="color:blue; background:lightblue; border: 5px solid black; width:80px; "> blue box </h5>

Using _object oriented_ styling you can change any of the properties in the `.blue` and `.box` _class_ attributes. Let's change the border color to green and increase its width to 20px from 5px.

```css
.blue.box {color:blue; border:20px solid black;}
```
<h5 style="color:blue; background:lightblue; border: 20px solid green; width:80px; "> blue box </h5>

In short, _object oriented_ styling (based on OOP) refers to using _CSS_ to modify chunks of _HTML_ sections (or "objects"). The goal is to use less code to change the design of a site. Refer to the overview of using the [CSS grid system](link)
