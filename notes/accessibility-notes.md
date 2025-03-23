---
title: Accessibility Notes
tags:
  - Accessibility
date: 2025-03-01
---
# Accessibility Notes

## Sources
https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA

## Accessibility Inspector (Firefox Developer Tools)
https://firefox-source-docs.mozilla.org/devtools-user/accessibility_inspector/index.html#check-for-accessibility-issues


## ARIA Overview
Accessible Rich Internet Applications (ARIA) is a set of roles and attributes that define ways to make web content and web applications (especially those developed with JavaScript) more accessible to people with disabilities.

It supplements HTML so that interactions and widgets commonly used in applications can be passed to assistive technologies when there is not otherwise a mechanism. For example, ARIA enables accessible JavaScript widgets, form hints and error messages, live content updates, and more.

### The First Rule of ARIA
The first rule of ARIA use is "If you can use a native HTML element or attribute with the semantics and behavior you require already built in, instead of re-purposing an element and adding an ARIA role, state or property to make it accessible, then do so.

### More Harm than Good?
There is a saying "No ARIA is better than bad ARIA." In WebAim's survey of over one million home pages, they found that Home pages with ARIA present averaged 41% more detected errors than those without ARIA. While ARIA is designed to make web pages more accessible, if used incorrectly, it can do more harm than good.

## ARIA Roles
ARIA roles provide semantic meaning to content, allowing screen readers and other tools to present and support interaction with an object in a way that is consistent with user expectations of that type of object. ARIA roles can be used to describe elements that don't natively exist in HTML or exist but don't yet have full browser support.

`region`
The region role is an ARIA landmark role. The region role should be reserved for sections of content sufficiently important that users will likely want to navigate to the section easily and to have it listed in a summary of the page. A region role is a more generic term, and should only be used if the section needing to be identified is not accurately described by one of the other landmark roles, such as banner, main, contentinfo, complementary, or navigation.

Every element with a region role should include a label that describes the purpose of the content in the region, preferably with an aria-labelledby referencing a visible header. If no visible appropriate header is present, aria-label should be used.

The region landmark role's content should make sense if separated from the main content of the document.

Using the <section> element will automatically communicate a section has a role of region if it is given an accessible name. Developers should always prefer using the correct semantic HTML element, in this case <section>, over using ARIA.

## Color Contrast
The contrast between the text and the background of a heading should be at least 4.5:1.

### Contrast Checker
https://webaim.org/resources/contrastchecker/
