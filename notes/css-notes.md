---
title: CSS Notes
tags:
  - CSS
date: 2025-02-10
---
# Notes on CSS0

## Kevin Powell - CSS Evangelist

### Website
https://www.kevinpowell.co/

### Videos
https://www.youtube.com/@KevinPowell/videos


## CSS Units
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

## Display

inline: Displays an element as an inline element (like ``<span>``). Any height and width properties will have no effect. This is default.
block: Displays an element as a block element (like ``<p>``). It starts on a new line, and takes up the whole width.
inline-block: Displays an element as an inline-level block container. The element itself is formatted as an inline element, but you can apply height and width values

## CSS Margins
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