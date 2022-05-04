# HTML Reference

My own (strongly opinionated) HTML (p)reference. Built from personal experience, the [MDN docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference), and the [Lighthouse tool](https://github.com/GoogleChrome/lighthouse#readme). Inspired by [AMPHTML](https://amp.dev/documentation/guides-and-tutorials/learn/spec/amphtml/).

## Inline Elements <!-- MDN: subset of Phrasing content category -->

Markup a single word or piece of text.

### `<i>`

- [Italic][mdn-i] emphasis
- [Use custom language](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i#usage_notes)
- Exists in markdown (`_ITALICS_`)

### `<b>`

- [Bold][mdn-b] emphasis
- [Highlight keywords](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b)
- Exists in markdown (`**BOLD**`)

## Elements <!-- MDN: subsets of Flow and Embedded content categories -->

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

### `<h1>`

- Allowed only once
- [Heading][mdn-headings] Webpage title
- Exists in Markdown `# HEADING`

### `<h2>` - `<h6>`

- [Heading][mdn-headings] Webpage section title
- Exists in Markdown `## HEADING` - `###### HEADING`

[mdn-i]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i
[mdn-b]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b
[mdn-div]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div
[mdn-p]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p
[mdn-ul]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul
[mdn-li]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li
[mdn-headings]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements
