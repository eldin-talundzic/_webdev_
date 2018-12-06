### Creating Lists

You can use lists to group information together. Lists are very commonly used (i.e menus, form elements, product info, etc)

###### Unordered list and nested list
```html
<ul>
<li> Item One </li>
<li> Item Two
    <ul>
      <li> 1.1 </li>
      <li> 1.2 </li>
    </ul>
</li>
<li> Item Three </li>
</ul>
```
> Output:
- Item One
- Item Two
  - 1.1
  - 1.2
- Item Three

###### Ordered lists
```html
<ol>
<li> Item One </li>
<li> Item Two
    <ol>
      <li> 1.1 </li>
      <li> 1.2 </li>
    </ol>
</li>
<li> Item Three <li>
</ol>
```
>output:
1. Item One
2. Item Two
  1. 1.1
  2. 1.2
3. Item Three

###### Customizing lists:
```html
<ol start="3" reversed>
<li> Item One </li>
<li> Item Two
    <ol type="i">
      <li> 1.1 </li>
      <li> 1.2 </li>
    </ol>
</li>
<li> Item Three <li>
</ol>
```
>Output:
> 3. Item One
> 2. Item Two
>     i. 1.1
>     ii. 1.2
> 1. Item Three

###### Description lists (definition lists) are the most flexible semantic elements in HTML5
> You can put more complicated structures within the definition description such as tables, paragraphs, etc. Definition lists are used for dialogue and glossaries often.

```html
<dl>
  <dt> Unordered lists </dt> <!-- description term -->
  <dd> Grouping in no order <dd> <!-- definition description-->
  <dt> Ordered lists </dt>
  <dd> Grouping in order <dd>
</dl>
```
>Output:
> **_Unordered lists_**
> &nbsp;&nbsp; Grouping in no order
> **_Ordered lists_**
> &nbsp;&nbsp; Grouping in order
