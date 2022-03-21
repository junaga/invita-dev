# HTML Reference

My own (strongly opinionated) [HTML](https://developer.mozilla.org/en-US/docs/Glossary/HTML) (p)reference. Built from personal experience, the [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference), the [AMPHTML docs](https://amp.dev/documentation/guides-and-tutorials/learn/spec/amphtml/) and the [Lighthouse tool](https://github.com/GoogleChrome/lighthouse#readme).

## Inline Elements <!-- MDN: subset of Phrasing content category -->

Markup a single word or piece of text.

<!--
- `<span>`
- `<q>`
  - Quote a paragraph
  - you can `cite` the quotes source URL
- `<code>`
  - snippets of computer language
  - exists in markdown
- `<br>`
-->

### `<i>`

- [Italic][mdn-i] emphasis
- [Use custom language](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i#usage_notes)
- Exists in markdown (`_ITALICS_`)

### `<b>`

- [Bold][mdn-b] emphasis
- [Highlight keywords](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b)
- Exists in markdown (`**BOLD**`)

## Elements <!-- MDN: subsets of Flow and Embedded content categories -->

<!--
- `<img>`
- `<svg>`
- `<audio>`
- `<video>`
- `<canvas>`
- `<iframe>`
- `<a>`
  -->

### `<div>`

- [Division][mdn-div] without semantic meaning
- Select content using CSS or JS

### `<p>`

- [Paragraph][mdn-p] of text
- Exists in Markdown (seperated by empty lines)

### `<ul>`

- [Unorderd List][mdn-ul] of `<li>` elements
- Exists in Markdown `- ITEM`

### `<li>`

- [List Item][mdn-li], from a set or array, of content
- Must be child of `<ul>`

## Sectioning Elements <!-- MDN: subsets Heading and Sectioning, content categories -->

Divide the page into sections/landmarks/an outline.

<!--
- `<section>`
- `<article>`
- `<aside>`
- `<nav>`
- `<header>`
- `<footer>`
-->

### `<h1>`

- Allowed only once
- [Heading][mdn-headings] Webpage title
- Exists in Markdown `# HEADING`

### `<h2>` - `<h6>`

- [Heading][mdn-headings] Webpage section title
- Exists in Markdown `## HEADING` - `###### HEADING`

<!--

## Meta Elements

Elements that are not descendents of `<body>`, they are not rendered.

## Global Attributes

Attributes valid on all elements, even the root `<html>`.

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
-->

[mdn-i]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i
[mdn-b]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b
[mdn-div]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div
[mdn-p]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p
[mdn-ul]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul
[mdn-li]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li
[mdn-headings]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements
[mdn-section]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section
[mdn-header]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header
[mdn-footer]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer
[mdn-q]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q
[mdn-code]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/code
