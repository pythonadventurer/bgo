---
title: HTML Notes
---
# HTML Notes

## Sources
https://www.freecodecamp.org/learn/2022/responsive-web-design/
https://developer.mozilla.org/en-US/docs/Web/HTML

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

## `<button>`
Both input and button elements are ``inline elements``, which don't appear on new lines.

For `submit` bttons, Add the type attribute with the value `submit` to the button to make it clear that it is a submit button.

Example:
```html
<button type="submit">Submit</button>
```

## `<fieldset>`
The fieldset element is used to group related inputs and labels together in a web form. fieldset elements are block-level elements, meaning that they appear on a new line.

The `<legend>` element acts as a caption for the content in the fieldset element

Example:
<fieldset>
    <legend>Is your cat an indoor or outdoor cat?</legend>
    <label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor"> Indoor</label>
    <label><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"> Outdoor</label>
</fieldset>
```

## `<figure>`
The figure element represents self-contained content with a caption.

Example:

```html
  <figure>
    <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/lasagna.jpg" alt="A slice of lasagna on a plate.">
    <figcaption>Cats love lasagna.</figcaption>  
  </figure>
```

## `<form>`

Form attributes:
`method`
`action`

Example of a complete form:

```html
<h1>Registration Form</h1>
<p>Please fill out this form with the required information</p>
<form method="post" action='https://register-demo.freecodecamp.org'>
    <fieldset>
    <label for="first-name">Enter Your First Name: <input id="first-name" name="first-name" type="text" required /></label>
    <label for="last-name">Enter Your Last Name: <input id="last-name" name="last-name" type="text" required /></label>
    <label for="email">Enter Your Email: <input id="email" name="email" type="email" required /></label>
    <label for="new-password">Create a New Password: <input id="new-password" name="new-password" type="password" pattern="[a-z0-5]{8,}" required /></label>
    </fieldset>
    <fieldset>
    <legend>Account type (required)</legend>
    <label for="personal-account"><input id="personal-account" type="radio" name="account-type" class="inline" checked /> Personal</label>
    <label for="business-account"><input id="business-account" type="radio" name="account-type" class="inline" /> Business</label>
    </fieldset>
    <fieldset>
    <label for="profile-picture">Upload a profile picture: <input id="profile-picture" type="file" name="file" /></label>
    <label for="age">Input your age (years): <input id="age" type="number" name="age" min="13" max="120" /></label>
    <label for="referrer">How did you hear about us?
        <select id="referrer" name="referrer">
        <option value="">(select one)</option>
        <option value="1">freeCodeCamp News</option>
        <option value="2">freeCodeCamp YouTube Channel</option>
        <option value="3">freeCodeCamp Forum</option>
        <option value="4">Other</option>
        </select>
    </label>
    <label for="bio">Provide a bio:
        <textarea id="bio" name="bio" rows="3" cols="30" placeholder="I like coding on the beach..."></textarea>
    </label>
    </fieldset>
    <legend>Did you have any positive experiences? Please check all that apply.</legend>
    <label for="terms-and-conditions">
        <input class="inline" id="terms-and-conditions" type="checkbox" /> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
    </label>
    <input type="submit" value="Submit" />
</form> 
```

## `<footer>`
The `footer` element is used to define a footer for a document or section. A footer typically contains information about the author of the document, copyright data, links to terms of use, contact information, and more.


## `<img>`
All `img` elements should have an `alt` attribute. The `alt` attribute's text is used for screen readers to improve accessibility and is displayed if the image fails to load.
Example:

```html
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="a cute orange cat">
```

## `<input>`
Input attributes:
`type`
`required`
`checked` (for check boxes)
`placeholder`
`pattern`

Input types:

### `checkbox`
For multiple checkboxes, give them all the same `name` attribute so only 1 may be checked at a time.

Form data for selected checkboxes are `name` / `value` attribute pairs. While the `value` attribute is optional, it's best practice to include it with any checkboxes or radio buttons on the page.

Example:
```html
<fieldset>
	<legend>What's your cat's personality?</legend>
	<input id="loving" type="checkbox" name="personality" value="loving"> <label for="loving">Loving</label>
	<input id="lazy" type="checkbox" name="personality" value="lazy"> <label for="lazy">Lazy</label>
	<input id="energetic" type="checkbox" name="personality" value="energetic"> <label for="energetic"> Energetic</label>
</fieldset>
```
### `email`
Example:

```html
<label for="email">Enter Your Email: <input id="email" name="email" type="email" required /></label>
```

### `password`
Example:

```html
<label for="new-password">Create a New Password: <input id="new-password" name="new-password" type="password" pattern="[a-z0-5]{8,}" required /></label>
```

### `radio`
Group multiple radio buttons within a `<fieldset>` element and gave them all the same `name` attribute to ensure only one may be chosen.

Example:

```html
<fieldset>
    <label for="business-account">
        <input id="business-account" type="radio" name="account-type" class="inline" checked /> Business
    </label>
    <label for="personal-account">
        <input id="personal-account" type="radio" name="account-type" class="inline" /> Personal
    </label>
</fieldset>
```

### `text`
Example:

```html
<label for="last-name">Enter Your Last Name: <input id="last-name" name="last-name" type="text" required /></label>
```

## `<label>`
label elements are used to help associate the text for an input element with the input element itself (especially for assistive technologies like screen readers).

Example:

```html
<label>
  <input type="radio"> Indoor
</label>
```

There's another way to associate an input element's text with the element itself. You can nest the text within a label element and add a for attribute with the same value as the input element's id attribute. 

Example:

```html
<input id="loving" type="checkbox">
<label for="loving">Loving</label>
```

## `<legend>`
The legend element acts as a caption for the content in the `<fieldset>` element. It gives users context about what they should enter into that part of the form. See: `<fieldset>`.


## `<main>`
The main element is used to represent the main content of the body of an HTML document. Content inside the main element should be unique to the document and should not be repeated in other parts of the document.

## `<ol>`
Ordered (numbered) list example:

<ol>
    <li>cat nip</li>
    <li>laser pointers</li>
    <li>lasagna</li>
</ol>

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

## `<ul>`
Unordered list example:

<ul>
    <li>cat nip</li>
    <li>laser pointers</li>
    <li>lasagna</li>
</ul>


# HTML Attributes

## `id`
The id attribute is used to identify specific HTML elements. Each id attribute's value must be unique from all other id values for the entire page.

The purpose of the ID attribute is to identify a single element when linking (using a fragment identifier), scripting, or styling (with CSS).


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

## `name`
Form data for input elements (such as checkboxes) consists of name / value pairs. See examples given for the `<input>`element.

## `value`
Defines a default value which will be displayed in the element on page load. 