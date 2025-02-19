---
title: CSS Reference Notes
tags:
  - CSS
date: 2025-02-10
---
# CSS Reference Notes

## Sources
- https://www.freecodecamp.org/learn/2022/responsive-web-design/
- https://developer.mozilla.org/en-US/docs/Web/CSS/
- https://www.w3schools.com/cssref


## Box Model
In the CSS box model, every HTML element is treated as a box with four areas:

- Content : the item in the box, such as a header, paragraph, or image element.
- Padding : the content is surrounded by a space called padding
- Border : encloses the padding and content.
- Margin : the area outside the box, used to control the space between elements.

## Comments in CSS
Example:
`/* comment here */`

## Flexbox
Flexbox is a one-dimensional CSS layout that can control the way items are spaced out and aligned within a container.

To use it, give an element a display property of `flex`. This will make the element a flex container. Any direct children of a flex container are called flex items.

### `flex-direction`
Flexbox has a main and cross axis. The main axis is defined by the `flex-direction` property, which has four possible values:

`row` (default) horizontal axis with flex items from left to right
`row-reverse` horizontal axis with flex items from right to left
`column` vertical axis with flex items from top to bottom
`column-reverse` vertical axis with flex items from bottom to top

Note: The axes and directions will be different depending on the text direction. The values shown are for a left-to-right text direction.

### `flex-wrap` 
Determines how flex items behave when the flex container is too small.  

`wrap` will allow the items to wrap to the next row or column. 
`nowrap` (default) will prevent items from wrapping and shrink them if needed.

### `justify-content`
Determines how the items inside a flex container are positioned along the main axis, affecting their position and the space around them.

### `align-items`
Positions the flex content along the cross axis. Example: if `flex-direction` is set to `row`, the cross axis is vertical.

### `object-fit`

`object-fit: cover` 
Fills the `img` container while maintaining aspect ratio, resulting in cropping to fit.

### `gap` 
Sets the gaps, also known as gutters, between rows and columns. The `gap` property and its `row-gap` and `column-gap` sub-properties provide this functionality for flex, grid, and multi-column layout. You apply the property to the container element.

The `::after` pseudo-element creates an element that is the last child of the selected element. You can use it to add an empty element after the last image. If you give it the same width as the images it will push the last image to the left when the gallery is in a two-column layout. Right now, it is in the center because you set `justify-content: center` on the flex container.


## Properties

### `align-items`

### `background-color`

### `background-image`

### `background`

### `blur`
The blur() CSS function applies a Gaussian blur to the input image. Its result is a `filter-function` 

Example:

```css
filter: blur(2px);
```

### `border`

### `border-bottom`

### `border-color`

### `border-left`

### `border-radius`
Rounds the corners of an element's outer border edge. You can set a single radius to make circular corners, or two radii to make elliptical corners.

### `box-shadow`
Adds shadow effects around an element's frame. You can set multiple effects separated by commas. A box shadow is described by X and Y offsets relative to the element, blur and spread radius, and color.

### `box-sizing`
Sets how the total width and height of an element is calculated.

By default in the CSS box model, the width and height you assign to an element is applied only to the element's content box. If the element has any border or padding, this is then added to the width and height to arrive at the size of the box that's rendered on the screen. This means that when you set width and height, you have to adjust the value you give to allow for any border or padding that may be added. For example, if you have four boxes with width: 25%;, if any has left or right padding or a left or right border, they will not by default fit on one line within the constraints of the parent container.

The `box-sizing` property can be used to adjust this behavior:

`content-box` gives you the default CSS box-sizing behavior. If you set an element's width to 100 pixels, then the element's content box will be 100 pixels wide, and the width of any border or padding will be added to the final rendered width, making the element wider than 100px.

`border-box` tells the browser to account for any border and padding in the values you specify for an element's width and height. If you set an element's width to 100 pixels, that 100 pixels will include any border or padding you added, and the content box will shrink to absorb that extra width. This typically makes it much easier to size elements.

`box-sizing: border-box` is the default styling that browsers use for the `<table>`, `<select>`, and `<button>` elements, and for `<input>` elements whose type is radio, checkbox, reset, button, submit, color, or search.

Note: It is often useful to set `box-sizing` to `border-box` to lay out elements. This makes dealing with the sizes of elements much easier, and generally eliminates a number of pitfalls you can stumble on while laying out your content. On the other hand, when using `position: relative` or `position: absolute`, use of `box-sizing: content-box` allows the positioning values to be relative to the content, and independent of changes to border and padding sizes, which is sometimes desirable.

### `color`

### `display`

`inline`       
Displays an element as an inline element (like ``<span>``). Any height and width properties will have no effect. This is default.

`block`
Displays an element as a block element (like ``<p>``). It starts on a new line, and takes up the whole width.

`inline-block` 
Displays an element as an inline-level block container. The element itself is formatted as an inline element, but height and width can e specified. If height and weight are omitted, `inline-block` elements only take up the width of their content.

If multiple `inline-block` items are on different lines, need to get them onn the same line to avoid extra whitespace between the objects.

#### Absolute Lengths
The absolute length units are fixed and a length expressed in any of these will appear as exactly that size.
Absolute length units are not recommended for use on screen, because screen sizes vary so much. However, they can be used if the output medium is known, such as for print layout.

`cm` Centimeters
`mm` Millimeters
`in` Inches (1in = 96px = 2.54cm)
`px` Pixels (1px = 1/96 of 1in) *
`pt` Points (1pt = 1/72 of 1in)
`pc` Picas (1pc = 12pt)

* Pixels (px) are relative to the viewing device. For low-dpi devices, 1px is one device pixel (dot) of the display. For printers and high resolution screens 1px implies multiple device pixels.

#### Relative Lengths
Relative length units specify a length relative to another length property. Relative length units scale better between different rendering medium.

`em`   Relative to the font-size of the element (2em means 2 times the size of the current font)	
`ex`   Relative to the x-height of the current font (rarely used)	
`ch`   Relative to the width of the "0" (zero)	
`rem`	 Relative to font-size of the root element	
`vw`   Relative to 1% of the width of the viewport*	
`vh` 	 Relative to 1% of the height of the viewport*	
`vmin` Relative to 1% of viewport's* smaller dimension	
`vmax` Relative to 1% of viewport's* larger dimension	
`%`	   Relative to the parent element

Tip: The `em` and `rem` units are practical in creating perfectly scalable layout!
* Viewport = the browser window size. If the viewport is 50cm wide, 1vw = 0.5cm.

### `filter`

### `flex-direction`
See [[#Flexbox]]

### `flex-wrap`
See [[#Flexbox]]

### `font-family`

### `font-size`

### `font-style`

### `gap`
See [[#Flexbox]]
### `height`

### `justify-content`
See [[#Flexbox]]

### `letter-spacing`
Used to adjust the space between each character of text in an element.

### `linear-gradient`

### `margin`
Used to create space around elements, outside of any defined borders. With CSS, you have full control over the margins. There are properties for setting the margin for each side of an element (top, right, bottom, and left).

#### Individual Sides
CSS has properties for specifying the margin for each side of an element:

`margin-top`
`margin-right`
`margin-bottom`
`margin-left`

All the margin properties can have the following values:

`auto`    : the browser calculates the margin
`length`  : specifies a margin in px, pt, cm, etc.
`%`       : specifies a margin in % of the width of the containing element
`inherit` : specifies that the margin should be inherited from the parent element

Negative values are allowed.
Setting `margin-left` and `margin-right` to `auto` centers the element within its parent element.

### `max-width`
Set `max-width` to prevent the element from being too wide on wider screen.

### `min-width`

### `object-fit`
See [[#Flexbox]]
### `overflow`

`overflow: hidden` is used to hide any content that overflows the bounds of an element, meaning that any content that exceeds the element's dimensions will not be visible. This is useful for preventing unwanted scrollbars and maintaining a clean layout.

### `padding-bottom`

### `padding`

### `rotate`

### `text-align`

### `text-transform`

### `transform `

### `vertical-align`

### `width`

Example:
Adjust the width so that `flavor` is 75% of the total width and `price` is 25%.

```html
<p class="flavor">Mocha</p><p class="price">4.50</p>
```

```css
.flavor {
  text-align: left;
  width: 75%;
}

.price {
    text-align: right;
    width: 25%
}
```