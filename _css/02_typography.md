
### CSS Typography

#### Web-Safe Fonts
Fonts that are installed on most computers or devices. See [CSS Font Stacks](https://www.cssfontstack.com). Remember to choose similar fonts and to provide at least **3** options (specific > more generic). For example:
```css
/* Choose similar fonts, separate options by commas,
provide last option with generic font */
h2 {
  font-family: "Helvetica Neue", Arial, sans-serif;
}
```
#### Web Fonts
**Internal source**
To provide your own fonts (assuming they are in the `fonts/` directory under your `project-name` directory) you will need to use the `@font-face {..}` declaration:

```css
@font-face{
  font-family: 'Museo Sans';
  src: url(../fonts/museo-sans.ttf);
}
```
**External source**
Requires no downloading of fonts. Link directly to high quality fonts. See [Google Fonts](https://fonts.google.com). Remember to add it to the `head` element, **before** the _CSS link_ in the _HTML_.
```html
<link href="https://fonts.googleapis.com/css?family=Caveat|Open+Sans" rel="stylesheet">
<link rel="stylesheet" href="/css/master.css">
```

#### Font Sizes
Different units for specifying font size(s):

| Font size type | Usage |
|----------------|-------|
| `px`           | absolute values, great for accuracy; always use whole numbers  |
| `em`           | calulated to nearest ancestor elements font size |
| `rem`          | calculated to the root element (i.e. `html`) font size |

See following link for font properties: [MDN Fonts](https://developer.mozilla.org/en-US/docs/Web/CSS/font).

#### Commonly used font style properties

| Font property  | Usage |
|----------------|-------|
| [line-height](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height) | adjust line height; use relative units (i.e. `em`). |
|[text-transform](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform)| how to capitalize text (i.e. `HeLLo`)
| [text-decoration](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/text-decoration) | `none; underline; overline; line-through; blink; inherit` |
|[text-align](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)| how text is aligned within parent element; only controls inline content (i.e. `a, span, strong`), not block content (i.e. `headings, div, p`) |


#### Icon Fonts
To include [Icon Fonts](https://fontawesome.com/?from=io), sign us using an email, get the CDN link and add it to the `head` of the HTML:
```html
<script type="text/javascript" src="link_provided_by_CDN"> </script>
```
> Check out font icon CDN (link above) for updated directions on how to use icons fonts. 
