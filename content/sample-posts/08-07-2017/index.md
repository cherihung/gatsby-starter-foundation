---
title: "More Flexbox, Header with Wrapping Lines"
cover: "https://unsplash.it/400/300/?random"
date: "08/07/2017"
category: "css3"
tags:
    - css
    - flexbox
---
Following the [previous post](/column-layout-using-flexbox/) on using [flexbox](http://css-tricks.com/snippets/css/a-guide-to-flexbox/) for page layout, here is one on using it to dictate position of page elements.

In the codepend example below, I created a header component similar to this [Line-On-Sides Header](http://css-tricks.com/line-on-sides-headers/) post from CSS-Tricks but by using flexbox. You should also check out the comments in that post for a variety of ways to approach the design. Flexbox is, by far, the simplest in terms of code needed.

No matter how the positioning is done. The most efficient way to draw the lines is utilizing the `:before` and `:after` pseudo-elements of the header container. Pseudo-elements are rendered as the container's children elements, on the same hierarchy as the title text itself.

In my example, that container is `<div class="title"></div>`.

##First, designate `.title` as a flex container. Then assign the proper flex attributes:##
```css
.title {
  display: flex; //make it flex!
  flex-direction: row; //line up the children elements horizontally
  align-items: center; //center children elements on the cross-axis AKA vertically
}
```
##Second, draw the lines:##
```css
.title:before, .title:after {
  content: " ";
  height: 0.2em; //this determines how far apart the lines are
  border-top: 1px solid #222; //line size and color
  border-bottom: 1px solid #222; //line size tne color
  width: 50%;
}
```
##That's it.##

*What does the last `width:50%` do exactly?* You must define a width so the pseudos will be drawn anyway. Each pseudo is 50% so the two will add up to 100% from end to end. Since they are flexbox children elements, they will be proportionally sized according to how large the title text is.

<p data-height="266" data-theme-id="10002" data-slug-hash="OPJvYq" data-default-tab="result" data-user="cherihung" class='codepen'>See the Pen <a href='http://codepen.io/cherihung/pen/OPJvYq/'>Layout and Decorative Header using Flexbox</a> by Chienyi Cheri Hung (<a href='http://codepen.io/cherihung'>@cherihung</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

**Few More Little Things**

As you can see, the title text in [my example](http://codepen.io/cherihung/pen/OPJvYq/) above is wrapped to two lines. That is flexbox fitting everything in a single row. But since there is no block width defined for the text, it'll shrink to wrap in favor of the block pseudos.

To make the title text a single line, you will need to apply some styles to the text itself. That is why I wrapped the text in a `<span>` tag in the first place, to have more direct control.

**1) designate the text itself to a table container:**
```css
.title span {
  display: table;
  margin: 0 10px; //add nice spacing between text and lines
}
```

The table element is not flexible (no pun intended). It will keep its width no matter what.

To make it all bit more visually pleasing, I added a `margin` to the left and right size of the text in this case. This will *push* the lines out of the container. You will want to add a `overflow: hidden` to `.title` to eliminate the overflowing visually.

**Or 2) give a width to the text:**

```css
.title span {
  width: 20%; //your choice of size and units. I prefer the fluid %.
}
```
With this treatment the text is fluid. Resize the browser and it will eventually wrap when the viewport is too narrow.
