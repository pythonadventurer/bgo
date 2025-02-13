---
title: CSS Notes
tags:
  - CSS
date: 2025-02-10
---
# Notes on CSS

## CSS Units
source: https://www.w3schools.com/cssref/css_units.php

### Absolute Lengths
The absolute length units are fixed and a length expressed in any of these will appear as exactly that size.
Absolute length units are not recommended for use on screen, because screen sizes vary so much. However, they can be used if the output medium is known, such as for print layout.

<table>
<tbody><tr>
<th>Unit</th>
<th>Description</th>
</tr>
<tr>
<td>cm</td>
<td>centimeters
</td>
</tr>
<tr>
<td>mm</td>
<td>millimeters
</td>
</tr>
<tr>
<td>in</td>
<td>inches (1in = 96px = 2.54cm)
</td>
</tr>
<tr>
<td>px *</td>
<td>pixels (1px = 1/96th of 1in)
</td>
</tr>
<tr>
<td>pt</td>
<td>points (1pt = 1/72 of 1in)
</td>
</tr>
<tr>
<td>pc</td>
<td>picas (1pc = 12 pt)
</td>
</tr>
</tbody></table>


### Relative Lengths
Relative length units specify a length relative to another length property. Relative length units scale better between different rendering medium.


<table >
  <tbody><tr>
    <th>Unit</th>
    <th>Description</th>
    <th></th>
  </tr>
  <tr>
    <td>em</td>
    <td>Relative to the font-size of the element (2em means 2 times the size of the current font)</td>
  </tr>
  <tr>
    <td>ex</td>
    <td>Relative to the x-height of the current font (rarely used)</td>
  </tr>
  <tr>
    <td>ch</td>
    <td>Relative to the width of the "0" (zero)</td>
  </tr>
  <tr>
    <td>rem</td>
    <td>Relative to font-size of the root element</td>
  </tr>
  <tr>
    <td>vw</td>
    <td>Relative to 1% of the width of the viewport*</td>
  </tr>
  <tr>
    <td>vh</td>
    <td>Relative to 1% of the height of the viewport*</td>
  </tr>
  <tr>
    <td>vmin</td>
    <td>Relative to 1% of viewport's* smaller dimension</td>
  </tr>
  <tr>
    <td>vmax</td>
    <td>Relative to 1% of viewport's* larger dimension</td>
  </tr>
  <tr>
    <td>%</td>
    <td>Relative to the parent element</td>
  </tr>
    </tbody></table>

## Display

| Value        | Description                                                                                                                                             |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| inline       | Displays an element as an inline element (like ``<span>``). Any height and width properties will have no effect. This is default.                       |
| block        | Displays an element as a block element (like ``<p>``). It starts on a new line, and takes up the whole width                                            |
| inline-block | Displays an element as an inline-level block container. The element itself is formatted as an inline element, but you can apply height and width values |
