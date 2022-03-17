# HTML Reference

My own (strongly opinionated) HTML (p)reference. Built from personal experience, the [MDN ref](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference), the [AMPHTML spec](https://amp.dev/documentation/guides-and-tutorials/learn/spec/amphtml/) and the [Lighthouse tool](https://github.com/GoogleChrome/lighthouse#readme).

1. [Elements](#elements) - In the viewport rendered, `<body>` child elements.
2. [Global Attributes](#global-attributes) - Attributes valid on all elements, even the root `<html>`.

## Elements

`<div>` [Division](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div)

- Generel purpose element
- Container for attributes or styles

### Sectioning elements

Devide elements into sections.

`<section>` - [Section](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section)

`<header>` - [Header](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header)

`<footer>` - [Footer](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer)

### Text content elements

Elements that display the written word.

`<p>` - [Paragraph](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p)

- exists in Markdown (has no statement/operator)

`<h1>`-`<h6>` - [Headings](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements)

- Headings of sections
- exists in Markdown

`<q>` - [Quote](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q)

- Quote a paragraph
- you can `cite` the quotes source URL

### Inline text elements

These elements are meant to be consumed inside "Text content elements" to give special semantic meaning to a short piece of text, or a single word. They should not have other child elements.

`<b>` [Bold](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b)

- Highlights keywords
- exists in markdown

`<i>` [Italic](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i)

- Represents custom language
- exists in markdown

`<code>` [Code](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/code)

- Indicates computer code
- exists in markdown

## Global Attributes

`class` [List of classes](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/class)

Each class name carries semantic meaning on it's own. They enhance the elements meaning, in order of appearence.

- lower-kebab-case-only. space as seperator
- Used as selector by CSS and Javascript

`id` [Unique ID](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/id)

- Link to an element, **within** the page
- lower-kebab-case-only
- Used as selector by CSS and Javascript

`lang` [Language](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/lang)

- Set the human language of elements
- `en-US`, `de`, etc

`dir` [Text Direction](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/dir)

- Set the text direction of elements
- `rtl` or `ltr`
