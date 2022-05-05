# HTML Reference

My own (strongly opinionated) HTML (p)reference. Built from personal experience, the [MDN docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference), and the [Lighthouse tool](https://github.com/GoogleChrome/lighthouse#readme). Inspired by [AMPHTML](https://amp.dev/documentation/guides-and-tutorials/learn/spec/amphtml/).

## Inline Elements

Markup a single word or piece of text. A subset of the [Phrasing content](https://html.spec.whatwg.org/multipage/dom.html#phrasing-content) category.

### `<q>`

- [Quote][mdn-q] something
- you can `cite="URL"` a source

### `<i>`

- [Italic][mdn-i] emphasis
- Use custom language
- Exists in markdown: `_ITALICS_`

### `<b>`

- [Bold][mdn-b] emphasis
- Highlight keywords
- Exists in markdown: `**BOLD**`

## Elements

### `<div>`

- [Division][mdn-div] without semantic meaning
- Select content using CSS or JS

### `<p>`

- [Paragraph][mdn-p] of text
- Exists in Markdown: (seperated by empty lines)

### `<ul>`

- [Unorderd List][mdn-ul] of `<li>` elements
- Exists in Markdown: `- ITEM`

### `<li>`

- [List Item][mdn-li], from a set or array, of content
- Must be child of `<ul>`

## Interactive Elements

A subset of the [Interactive content](https://html.spec.whatwg.org/multipage/dom.html#interactive-content) category.

### `<a href="URL">`

- [Anchor. Hyper-reference][mdn-a] URLs
- `download` the resource instead
- add `target="_blank"` to open in a new tab
- Exists in markdown - `[TEXT](URL)`

## Sectioning Elements

Divide the page into sections/landmarks/an outline.

### `<h1>`

- Allowed only once
- [Heading][mdn-headings] Webpage title
- Exists in Markdown: `# HEADING`

### `<h2>` - `<h6>`

- [Heading][mdn-headings] section title
- Exists in Markdown `## HEADING` - `###### HEADING`

## Elements I don't use,

and their suggested alternative in semantics (HTML).
Including of course, all [deprecated Elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element#obsolete_and_deprecated_elements).

- `<em>` - prefer: `<i>`
- `<strong>` - prefer: `<b>`
- `<u>` - prefer `<mark>`
- `<blockquote>` - prefer `<q>`
- `<ol>` - prefer `<ul>`

[mdn-a]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a
[mdn-q]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q
[mdn-i]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i
[mdn-b]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b
[mdn-div]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div
[mdn-p]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p
[mdn-ul]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul
[mdn-li]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li
[mdn-headings]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements
