#### Responsive Design

Responsive design aims to be device agnostic, optimized for any screen size using [@media](https://www.w3schools.com/css/css_rwd_mediaqueries.asp) rules. See
[Media Queries](https://mediaqueri.es): responsive website design for examples.
Follow progressive enhancement development:
- Focus on developing content for mobile-first
- Reduce reliance on mouse actions, add touch friendly interaction instead
- Focus on content loading quickly and for smaller screens
- Plan all of the content and design at the beginning (focus only on essentials)
- Add enhancements later, if needed

Review the difference between `adaptive`, `responsive`, `static` and `liquid` designs at [Liquidapsive](http://www.liquidapsive.com).

Add fluid (flexible) CSS before adding media queries for responsive design.
To create a flexible layout:
- Use `%` based widths for page components
- Use `min` and `max-width` to add constraints to layouts
- Use `%` `min` and `max` values together

Consider the following example:

```html
<div class="content-wrap">
  <p>
    Lorem Ipsum has been the industry's standard dummy text ever since the
    1500s, when an unknown printer took a galley of type and scrambled it to
    make a type specimen book. It has survived not only five centuries, but
    also the leap into electronic typesetting, remaining essentially unchanged.
    It was popularised in the 1960s with the release of Letraset sheets
    containing Lorem Ipsum passages, and more recently with desktop publishing
    software like Aldus PageMaker including versions of Lorem Ipsum.
  </p>
</div>
```

```css
.content-wrap {
  background: rgba(47,79,79,0.2);
  padding: 20px;
  line-height: 1.5;

  /* Center the container and content to the page */
  margin: 0 auto;

  /* Make container flexible that maxes out at 400px */
  max-width: 400px;
  /* If viewport is smaller than 400px, content will be 60% of its container */
  width: 60%;
}
```
Flexible layout are relative. The content and components only get wider or narrower, as in the above example. In comparison, responsive layouts change based on size of the viewport (e.g., 2 column content > 4 column content). Adding a fluid layout beforehand, however, will help with responsive design.

See [media queries, types and features](https://tympanus.net/codrops/css_reference/media-queries/). The `@media [not | only] <media-type> [and] (<media-codntion>);` provide the `if-else` statements for the browser to interpret.

In responsive design, the `width` feature is most predominantly used. The `min-width:` and `max-width:` are used to designate equal to greater than or equal to or less than conditions.

Media queries can be added using the `<link>` tag to select only specific CSS to load.
The below example, will only load the `mobile.css` only if viewport is equal to 600px or less.

```html
<link media="screen and (max-width:600px)" rel="stylesheet" href="/css/mobile.css">
```
Alternatively, `@media queries` can be added in the CSS to apply specific conditions to styles:

```css
/* If not specified, will be applied to all */
@media (max-width:600px) {
  /* regular CSS goes here */
  .selector {
    ...
  }
}
```
If the `@media <media-type>` is not specified, it will apply it to all devices. Alternatively, you can specify a type:

| type | usage |
|--------------------|-------|
| `all` | all devices |  
| `print` | printers and/or printed displays |  
| `screen` | all devices not matched by print or speech |
| `speech` | screen readers and devices that "read out" a page |

To specify specific breakpoints using `min-width` and `max-width` separate them using a `1px` difference. Otherwise the second media query will override the first. For example:
```css
/* Extra small devices (phones, 600px and down) */
@media (max-width:600px) {
.selector { ...}
}

/* Small devices (600px and up) */
@media (min-width:601) {
.selector { ...}
}
```
To specify a range that will apply specified style to 800px or larger screens and screens less than 1200px. 
```css
/* target 800px up to 1200px */  
@media (min-width: 800px) and (max-width:600px) {
.selector { ...}
}

```
