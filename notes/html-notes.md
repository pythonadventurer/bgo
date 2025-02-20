---
title: HTML Notes
---

# HTML Page Template

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <link rel="stylesheet" href="styles.css">    
    <title>Title</title>
   
</head>

<body>
<img src="" alt="description">

</body>

</html>
```

# HTML Comments
Example:

```html
<!-- TODO: Add link to cat photos -->
```

# HTML Elements
HTML5 has some elements that identify different content areas. These elements make HTML easier to read and help with Search Engine Optimization (SEO) and accessibility.

Nested elements should be placed two spaces further to the right of the element they are nested in. This spacing is called indentation and it is used to make HTML easier to read.

## `<a>`
Anchor element. Link to another page. Place text between the open and closing tags of the `<a>` element. Example:

```html
<a href="https://www.freecodecamp.org">click here to go to freeCodeCamp</a>
```

Example of link text in a paragraph:

```html
<p>See more <a href="https://freecatphotoapp.com">cat photos</a> in our gallery.<p>
```

Use `target=blank` to open a link in a new tab. Example:

```html
<a href="https://www.freecodecamp.org" target="_blank">freeCodeCamp</a>
```

Turn content into a link by wrapping it in an anchor element. Example:

```html
<a href="https://freecatphotoapp.com">
  <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back.">
</a>
```

## `<article>`
Article elements commonly contain multiple elements that have related information.

## `<img>`
All `img` elements should have an `alt` attribute. The `alt` attribute's text is used for screen readers to improve accessibility and is displayed if the image fails to load.
Example:

```html
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="a cute orange cat">
```

## `<main>`
The main element is used to represent the main content of the body of an HTML document. Content inside the main element should be unique to the document and should not be repeated in other parts of the document.

## `<section>`
The section element is used to define sections in a document, such as chapters, headers, footers, or any other sections of the document. It is a semantic element that helps with SEO and accessibility.

When you add a lower rank heading element to the page, it's implied that you're starting a new subsection.

Example:

```html
<section>
    <h2>Cat Lists</h2>
        <h3>Things cats love:</h3>
</section>
```

# HTML Attributes

## `id`
Targeted in css with `#`.  Example:

```html
<div id="cat"></div>
```

```css
#cat {

}
```

## `class`
Targeted in css with `.` Example:

```html
<div class="cat"></div>
```

```css
.cat {

}
```

