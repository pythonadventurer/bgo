---
title: Learn CSS by Building a Set of Colored Markers
tags:
  - CSS
source: Learn CSS by Building a Set of Colored Markers
---
# Learn CSS by Building a Set of Colored Markers

Misc. notes

## Step 13
Your marker would look better if it was centered on the page. An easy way to do that is with the margin shorthand property.

In the last project, you set the margin area of elements separately with properties like margin-top and margin-left. The margin shorthand property makes it easy to set multiple margin areas at the same time.

## Step 15
While you have three separate marker `div` elements, they look like one big rectangle. You should add some space between them to make it easier to see each element.

When the shorthand `margin` property has two values, it sets `margin-top` and `margin-bottom` to the first value, and `margin-left` and `margin-right` to the second value.

In your `.marker` CSS rule, set the `margin` property to `10px auto`.

```css
.marker {
  width: 200px;
  height: 25px;
  background-color: red;
  margin: 10px auto; 
}
```

## Step 21 About RGB

There are two main color models: the additive RGB (red, green, blue) model used in electronic devices, and the subtractive CMYK (cyan, magenta, yellow, black) model used in print.

In this project, you'll work with the RGB model. This means that colors begin as black, and change as different levels of red, green, and blue are introduced. An easy way to see this is with the CSS `rgb` function.

Create a new CSS rule that targets the class `container` and set its `background-color` to black with `rgb(0, 0, 0)`.


## Step 25 - Padding top and bottom
Now add a little more vertical space between your markers and the edge of the `container` element they're in.

In the `.container` CSS rule, use the shorthand `padding` property to add `10px` of top and bottom padding, and set the left and right padding to `0`. This works similarly to the shorthand `margin` property you used earlier.

## Step 28 - Secondary Colors
Secondary colors are the colors you get when you combine primary colors. You might have noticed some secondary colors in the last step as you changed the red, green, and blue values.

To create the first secondary color, yellow, update the `rgb` function in the `.one` CSS rule to combine pure red and pure green.

## Step 29 - Cyan
To create the next secondary color, cyan, update the rgb function in the .two CSS rule to combine pure green and pure blue.

## Step 31 - Tertiary Colors
Now that you're familiar with secondary colors, you'll learn how to create tertiary colors. Tertiary colors are created by combining a primary with a nearby secondary color.

To create the tertiary color orange, update the rgb function in the .one CSS rule so that red is at the max value, and set green to 127.

## Step 37 - Dominant vs Accent Color
Notice that the red and cyan colors are very bright right next to each other. This contrast can be distracting if it's overused on a website, and can make text hard to read if it's placed on a complementary-colored background.

It's better practice to choose one color as the dominant color, and use its complementary color as an accent to bring attention to certain content on the page.

First, in the `h1` rule, use the `rgb` function to set its `background-color` to cyan.

## Step 39 - Drawing Attention

Notice how your eyes are naturally drawn to the red color in the center? When designing a site, you can use this effect to draw attention to important headings, buttons, or links.

There are several other important color combinations outside of complementary colors, but you'll learn those a bit later.

For now, use the rgb function in the .two CSS rule to set the background-color to black.

## Step 46 Using Hex Colors

A very common way to apply color to an element with CSS is with hexadecimal or hex values. While hex values sound complicated, they're really just another form of RGB values.

Hex color values start with a # character and take six characters from 0-9 and A-F. The first pair of characters represent red, the second pair represent green, and the third pair represent blue. For example, ``#4B5320``.

In the .green class selector, set the background-color property to a hex color code with the values 00 for red, FF for green, and 00 blue.

## Step 47 Hexadecimal Numbers

You may already be familiar with decimal, or base 10 values, which go from 0 - 9. Hexadecimal, or base 16 values, go from 0 - 9, then A - F:

Example Code

```js
0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F
```

With hex colors, `00` is 0% of that color, and `FF` is 100%. So `#00FF00` translates to 0% red, 100% green, and 0% blue, and is the same as `rgb(0, 255, 0)`.

Lower the intensity of green by setting the green value of the hex color to `7F`.

## Step 48 - The HSL Color Model
The HSL color model, or hue, saturation, and lightness, is another way to represent colors.

The CSS hsl function accepts 3 values: a number from 0 to 360 for hue, a percentage from 0 to 100 for saturation, and a percentage from 0 to 100 for lightness.

If you imagine a color wheel, the hue red is at 0 degrees, green is at 120 degrees, and blue is at 240 degrees.

Saturation is the intensity of a color from 0%, or gray, to 100% for pure color. You must add the percent sign % to the saturation and lightness values.

Lightness is how bright a color appears, from 0%, or complete black, to 100%, complete white, with 50% being neutral.

In the .blue CSS rule, use the hsl function to change the background-color property to pure blue. Set the hue to 240, the saturation to 100%, and the lightness to 50%.

Example:

```css
.blue {
  background-color: hsl(240,100%,50%);
}
```

## Step 49 - Gradient
You've learned a few ways to set flat colors in CSS, but you can also use a color transition, or gradient, on an element.

A gradient is when one color transitions into another. The CSS `linear-gradient` function lets you control the direction of the transition along a line, and which colors are used.

One thing to remember is that the `linear-gradient` function actually creates an `image` element, and is usually paired with the `background` property which can accept an image as a value.

In the `.red` CSS rule, change the `background-color` property to `background`.

## Step 50 - linear-gradient function

The linear-gradient function is very flexible -- here is the basic syntax you'll use in this tutorial:

### Example Code

```css
linear-gradient(gradientDirection, color1, color2, ...);
```

gradientDirection is the direction of the line used for the transition. color1 and color2 are color arguments, which are the colors that will be used in the transition itself. These can be any type of color, including color keywords, hex, rgb, or hsl.

Now you'll apply a red-to-green gradient along a 90 degree line to the first marker.

First, in the .red CSS rule, set the background property to linear-gradient(), and pass it the value 90deg as the gradientDirection.

Result:

```css
.red {
  background: linear-gradient(90deg, rgb(255, 0, 0), rgb(0,255,0));
}
```

## Step 53 - Gradient with Three Colors

```css
.red {
  background: linear-gradient(90deg, rgb(255, 0, 0), rgb(0, 255, 0), rgb(0,0,255));
}
```

## Step 54
Color-stops allow you to fine-tune where colors are placed along the gradient line. They are a length unit like `px` or percentages that follow a color in the `linear-gradient` function.

For example, in this red-black gradient, the transition from red to black takes place at the 90% point along the gradient line, so red takes up most of the available space:

Example Code

```css
linear-gradient(90deg, red 90%, black);
```

In the `linear-gradient` function, add a `75%` color stop after the first red color argument. Do not add color stops to the other colors arguments.


## Step 64

Even without the color-stops, you might have noticed that the colors for the green marker transition at the same points as the red marker. The first color is at the start (0%), the second is in the middle (50%), and the last is at the end (100%) of the gradient line.

The linear-gradient function automatically calculates these values for you, and places colors evenly along the gradient line by default.

In the .red CSS rule, remove the three color stops from the linear-gradient function to clean up your code a bit.


# Step 75

You're already familiar with using the `rgb` function to set colors. To add an alpha channel to an `rgb` color, use the `rgba` function instead.

The `rgba` function works just like the `rgb` function, but takes one more number from `0` to `1.0` for the alpha channel:

Example Code

```css
rgba(redValue, greenValue, blueValue, alphaValue);
```

You can also use an alpha channel with `hsl` and `hex` colors. You will see how to do that soon.

In the `.sleeve` rule, use the `rgba` function to set the `background-color` property to pure white with 50% opacity.


## Step 78

It looks like your sleeve disappeared, but don't worry -- it's still there. What happened is that your new cap div is taking up the entire width of the marker, and is pushing the sleeve down to the next line.

This is because the default display property for div elements is block. So when two block elements are next to each other, they stack like actual blocks. For example, your marker elements are all stacked on top of each other.

To position two div elements on the same line, set their display properties to inline-block.

Create a new rule to target both the cap and sleeve classes, and set display to inline-block.


## Step 79

In the last project, you learned a little bit about borders and the border-color property.

All HTML elements have borders, though they're usually set to none by default. With CSS, you can control all aspects of an element's border, and set the border on all sides, or just one side at a time. For a border to be visible, you need to set its width and style.

In the .sleeve CSS rule, add the border-left-width property with the value 10px.

## Step 86

The last thing you'll do is add a slight shadow to each marker to make them look even more realistic.

The box-shadow property lets you apply one or more shadows around an element. Here is basic syntax:
Example Code

box-shadow: offsetX offsetY color;

Here's how the offsetX and offsetY values work:

- both offsetX and offsetY accept number values in px and other CSS units
- a positive offsetX value moves the shadow right and a negative value moves it left
- a positive offsetY value moves the shadow down and a negative value moves it up
- if you want a value of zero (0) for any or both offsetX and offsetY, you don't need to add a unit. Every browser understands that zero means no change.

The height and width of the shadow is determined by the height and width of the element it's applied to. You can also use an optional spreadRadius value to spread out the reach of the shadow. More on that later.

Start by adding a simple shadow to the red marker.

In the .red CSS rule, add the box-shadow property with the values 5px for offsetX, 5px for offsetY, and red for color.


# Step 88

Notice that the edges of the shadow are sharp. This is because there is an optional `blurRadius` value for the `box-shadow` property:

Example Code

```css
box-shadow: offsetX offsetY blurRadius color;
```

If a `blurRadius` value isn't included, it defaults to `0` and produces sharp edges. The higher the value of `blurRadius`, the greater the blurring effect is.

In the `.green` CSS rule, add the `box-shadow` property with the values `5px` for `offsetX`, `5px` for `offsetY`, `5px` for `blurRadius`, and `green` for `color`.

## Step 89

But what if you wanted to expand the shadow out further? You can do that with the optional spreadRadius value:
Example Code

```css
box-shadow: offsetX offsetY blurRadius spreadRadius color;
```

Like blurRadius, spreadRadius defaults to 0 if it isn't included.

Practice by adding a 5 pixel shadow directly around the blue marker.

In the .blue CSS rule, add the box-shadow property with the values 0 for offsetX, 0 for offsetY, 0 for blurRadius, 5px for spreadRadius, and blue for color.
