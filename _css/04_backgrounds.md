#### Background Property

The [background](https://developer.mozilla.org/en-US/docs/Web/CSS/background) property is a shorthand method for styling multiple options at once, including [background-clip](https://developer.mozilla.org/en-US/docs/Web/CSS/background-clip), [background-color](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color), [background-image](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color), [background-origin](https://developer.mozilla.org/en-US/docs/Web/CSS/background-origin), [background-position](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position), [background-repeat](https://developer.mozilla.org/en-US/docs/Web/CSS/background-repeat), [background-size](https://developer.mozilla.org/en-US/docs/Web/CSS/background-size), and [background-attachment](https://developer.mozilla.org/en-US/docs/Web/CSS/background-attachment).

Consider the following:

```css
selector {
  background-color:green;
  background-position: top bottom; /* can also use 0px 0px */
  background-repeat: no-repeat;
  background-image: url(image.jpg);
  background-size: cover;
  background-clip: content-box;
  background-origin: border-box;
}

/* You can also use shorthand with space in between parameters; background size requires a `/` only */
/* Background size must follow after background position */
selector {
  background: green url(image.jpg) no-repeat fixed 0px 0px / cover;
}
```

#### RGB & Alpha Transparency

Use `background: rgba(n,n,n,n)` to add alpha transparency using a color and/or two background images. See examples below:

```html
<div class="img-bg">
  <div class="alpha-bg">
    <p>
    Lorem Ipsum is simply dummy text of the printing and typesetting industry.
    Lorem Ipsum has been the industry's standard dummy text ever since the
    1500s, when an unknown printer took a galley of type and scrambled it to
    make a type specimen book. It has survived not only five centuries, but
    also the leap into electronic typesetting, remaining essentially unchanged.
    It was popularised in the 1960s with the release of Letraset sheets
    containing Lorem Ipsum passages, and more recently with desktop publishing
    software like Aldus PageMaker including versions of Lorem Ipsum.  
    </p>
  </div>
</div>
```

```css
/* Color resource: http://colours.neilorangepeel.com */

.img-bg {
  width: 600px;
  font-family: Helvetica, Arial, sans-serif;
  line-height:1.5;
  background: url(https://source.unsplash.com/random) no-repeat;
}

.alpha-bg {
  padding:20px;
  height:100%;
  color: white;

  /* add color with rgb alpha transparency to image */
  /* color1, color2, color3, alpha */
  /* This works only since the alpha-bg is nested in the img-bg div
  since its higher on the stack (z-index) */
  background: rgba(70,130,180, 0.8);
}
```
If you have only one element (i.e. `image`) and want to add alpha transparency to it using two color schemes via a gradient, use the the [liniear-gradient](https://developer.mozilla.org/en-US/docs/Web/CSS/linear-gradient) css function:

```html
<div class="img-bg">
<p>Lorem Ipsum is simply dummy text of the printing and typesetting industry.
    Lorem Ipsum has been the industry's standard dummy text ever since the
    1500s, when an unknown printer took a galley of type and scrambled it to
    make a type specimen book. It has survived not only five centuries, but
    also the leap into electronic typesetting, remaining essentially unchanged.
    It was popularised in the 1960s with the release of Letraset sheets
    containing Lorem Ipsum passages, and more recently with desktop publishing
    software like Aldus PageMaker including versions of Lorem Ipsum. </p>
</div>
```
```css
.img-bg {
  width: 500px;
  font-family: Helvetica, Arial, sans-serif;
  line-height:1.5;

  background: linear-gradient(rgba(70,130,180, 0.8), rgba(72,209,204, 0.2)),
  url(https://source.unsplash.com/random);    
}
```

Now lets combine all this to create a parallax scrolling background.

```html
<div style="font-size:16px">
 Scroll Up and Down this page to see the parallax scrolling effect.
This div is just here to enable scrolling.
</div>

<div class="img-bg">
  <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry.
 </p>
</div>

<div class="img-bg">
  <p>Lorem Ipsum is simply dummy text of the printing and   typesetting industry.
  </p>
</div>

 <div style="height:600px;font-size:16px">
 Scroll Up and Down this page to see the parallax scrolling effect.
This div is just here to enable scrolling.
Tip: Try to remove the background-attachment property to remove the scrolling effect.
</div>
```

```css
.img-bg {
  height: auto;         /* turn to auto to keep image scale, make it responsive */
  min-height:200px;
  width:100%;           /* add for responsive scaling */

  /* If you want an image to scale down if it has to, but never scale up
  to be larger than its original size then use:
  height:100%; */

  font-family: Helvetica, Arial, sans-serif;
  line-height:1.5;
  color:white;

  background: linear-gradient(rgba(70,130,180, 0.4), rgba(72,209,204, 0.2)),
  url(https://source.unsplash.com/random) fixed center no-repeat / cover;
}
```
Test out above code using: [JSfiddle](https://jsfiddle.net/)
