---
title: CSS Notes
tags:
  - CSS
date: 2025-02-10
---
# Notes on CSS

## Kevin Powell - CSS Evangelist

### Website
https://www.kevinpowell.co/

### Videos
https://www.youtube.com/@KevinPowell/videos

## Box Model
In the CSS box model, every HTML element is treated as a box with four areas:

- Content : the item in the box, such as a header, paragraph, or image element.
- Padding : the content is surrounded by a space called padding
- Border : encloses the padding and content.
- Margin : the area outside the box, used to control the space between elements.

## Border Radius
*Source: https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius*

The border-radius CSS property rounds the corners of an element's outer border edge. You can set a single radius to make circular corners, or two radii to make elliptical corners.

### Examples

```css
/* The syntax of the first radius allows one to four values */
/* Radius is set for all 4 sides */
border-radius: 10px;

/* top-left-and-bottom-right | top-right-and-bottom-left */
border-radius: 10px 5%;

/* top-left | top-right-and-bottom-left | bottom-right */
border-radius: 2px 4px 2px;

/* top-left | top-right | bottom-right | bottom-left */
border-radius: 1px 0 3px 4px;

/* The syntax of the second radius allows one to four values */
/* (first radius values) / radius */
border-radius: 10px / 20px;

/* (first radius values) / top-left-and-bottom-right | top-right-and-bottom-left */
border-radius: 10px 5% / 20px 30px;

/* (first radius values) / top-left | top-right-and-bottom-left | bottom-right */
border-radius: 10px 5px 2em / 20px 25px 30%;

/* (first radius values) / top-left | top-right | bottom-right | bottom-left */
border-radius: 10px 5% / 20px 25em 30px 35em;

/* Global values */
border-radius: inherit;
border-radius: initial;
border-radius: revert;
border-radius: revert-layer;
border-radius: unset;

```



## Box Shadow
*source: https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow*

The box-shadow CSS property adds shadow effects around an element's frame. You can set multiple effects separated by commas. A box shadow is described by X and Y offsets relative to the element, blur and spread radius, and color.

Examples:

```css
/* Keyword values */
box-shadow: none;

/* A color and two length values */
/* <color> | <length> | <length> */
box-shadow: red 60px -16px;

/* Three length values and a color */
/* <length> | <length> | <length> | <color> */
box-shadow: 10px 5px 5px black;

/* Four length values and a color */
/* <length> | <length> | <length> | <length> | <color> */
box-shadow: 2px 2px 2px 1px rgb(0 0 0 / 20%);

/* inset, length values, and a color */
/* <inset> | <length> | <length> | <color> */
box-shadow: inset 5em 1em gold;

/* Any number of shadows, separated by commas */
box-shadow:
  3px 3px red inset,
  -1em 0 0.4em olive;

/* Global values */
box-shadow: inherit;
box-shadow: initial;
box-shadow: revert;
box-shadow: revert-layer;
box-shadow: unset;

```

## Display
inline: Displays an element as an inline element (like ``<span>``). Any height and width properties will have no effect. This is default.
block: Displays an element as a block element (like ``<p>``). It starts on a new line, and takes up the whole width.
inline-block: Displays an element as an inline-level block container. The element itself is formatted as an inline element, but you can apply height and width values

## Units
source: https://www.w3schools.com/cssref/css_units.php

### Absolute Lengths
The absolute length units are fixed and a length expressed in any of these will appear as exactly that size.
Absolute length units are not recommended for use on screen, because screen sizes vary so much. However, they can be used if the output medium is known, such as for print layout.

cm: Centimeters
mm: Millimeters
in: Inches (1in = 96px = 2.54cm)
px: Pixels (1px = 1/96 of 1in)
pt: Points (1pt = 1/72 of 1in)
pc: Picas (1pc = 12pt)

* Pixels (px) are relative to the viewing device. For low-dpi devices, 1px is one device pixel (dot) of the display. For printers and high resolution screens 1px implies multiple device pixels.

### Relative Lengths
Relative length units specify a length relative to another length property. Relative length units scale better between different rendering medium.

em:   Relative to the font-size of the element (2em means 2 times the size of the current font)	
ex:	  Relative to the x-height of the current font (rarely used)	
ch:	  Relative to the width of the "0" (zero)	
rem:	Relative to font-size of the root element	
vw:	  Relative to 1% of the width of the viewport*	
vh: 	Relative to 1% of the height of the viewport*	
vmin:	Relative to 1% of viewport's* smaller dimension	
vmax:	Relative to 1% of viewport's* larger dimension	
%	Relative to the parent element

Tip: The em and rem units are practical in creating perfectly scalable layout!
* Viewport = the browser window size. If the viewport is 50cm wide, 1vw = 0.5cm.

## Filter

### Blur
*Source: https://developer.mozilla.org/en-US/docs/Web/CSS/filter-function/blur*

The blur() CSS function applies a Gaussian blur to the input image. Its result is a <filter-function>. Example:

```
filter: blur(2px);
```



## Margin
*Source: https://www.w3schools.com/css/css_margin.asp*

The CSS margin properties are used to create space around elements, outside of any defined borders.
With CSS, you have full control over the margins. There are properties for setting the margin for each side of an element (top, right, bottom, and left).

### Margin - Individual Sides
CSS has properties for specifying the margin for each side of an element:

- margin-top
- margin-right
- margin-bottom
- margin-left

All the margin properties can have the following values:

- auto - the browser calculates the margin
- length - specifies a margin in px, pt, cm, etc.
- % - specifies a margin in % of the width of the containing element
- inherit - specifies that the margin should be inherited from the parent element

Tip: Negative values are allowed.

## Overflow
The CSS property overflow: hidden; is used to hide any content that overflows the bounds of an element, meaning that any content that exceeds the element's dimensions will not be visible. This is useful for preventing unwanted scrollbars and maintaining a clean layout.

## Transform
*Source: https://developer.mozilla.org/en-US/docs/Web/CSS/transform*

The transform CSS property lets you rotate, scale, skew, or translate an element. It modifies the coordinate space of the CSS visual formatting model.

### Examples

```css
/* Keyword values */
transform: none;

/* Function values */
transform: matrix(1, 2, 3, 4, 5, 6);
transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
transform: perspective(17px);
transform: rotate(0.5turn);
transform: rotate3d(1, 2, 3, 10deg);
transform: rotateX(10deg);
transform: rotateY(10deg);
transform: rotateZ(10deg);
transform: translate(12px, 50%);
transform: translate3d(12px, 50%, 3em);
transform: translateX(2em);
transform: translateY(3in);
transform: translateZ(2px);
transform: scale(2, 0.5);
transform: scale3d(2.5, 1.2, 0.3);
transform: scaleX(2);
transform: scaleY(0.5);
transform: scaleZ(0.3);
transform: skew(30deg, 20deg);
transform: skewX(30deg);
transform: skewY(1.07rad);

/* Multiple function values */
transform: translateX(10px) rotate(10deg) translateY(5px);
transform: perspective(500px) translate3d(10px, 0, 20px) rotateY(30deg);

/* Global values */
transform: inherit;
transform: initial;
transform: revert;
transform: revert-layer;
transform: unset;

```

