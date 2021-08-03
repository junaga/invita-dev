# HTML Reference

My own (strongly opinionated) HTML (p)reference of **elements** and **attributes**. Built from personal experience, the [MDN ref](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference) and the [AMPHTML spec](https://github.com/ampproject/amphtml/blob/main/docs/spec/amp-html-format.md). Grouped into three sections:

1. [Elements](#Elements) - In the visible viewport rendered, `<body>` child elements.
2. [Global Attributes](#Global-Attributes) - Attributes valid on all elements, even the root `<html>`.
3. [Meta and misc](#Meta-and-misc) - Metadata `<head>` child elements and other miscellaneous things.

## Elements

#### `<div>` Division

The generel purpose element, or container for attributes. If there exists a semantically more meaningfull element it should be used.

### Text content elements

Elements that display the written word.

#### `<p>` Paragraph

- exists in Markdown (has no statement/operator)

#### `<h1>` - `<h6>` Heading

- Heading of sections
- exists in Markdown

#### `<blockquote>` Block Quotation

- quote entire paragraphs
- exists in Markdown
- you can `cite` the quotes source URL

### Inline text elements

These elements are meant to be consumed inside "Text content elements" to give special semantic meaning to a short piece of text, or a single word. They should not have other child elements.

### `<b>` Bold

- Highlights keywords
- exists in markdown

Bold is better then caps.

### `<i>` Italic

- Represents custom language
- exists in markdown

### Sectioning elements

Multiple elements combined should be grouped by sections, using these _sectioning elements_.

### `<main>` Main

- Should be used only once
- Represents the dominent and unique content of the document

### `<section>` Section

Generel purpose sectioning element, like `<div>` but for document structure. If there exists a semantically more meaningfull element it should be used.

## Meta and misc

HTML `<!-- comments -->` can be used **anywhere**. Conditional comments are not allowed.

Use these **HTML Entities** to escape reserved HTML characters:

- `&lt;` for `<`
- `&gh;` for `>`
- `&quot;` for `"`
- `&amp;` for `&`

### `<html>` Document

- Allowed only once, as the root element in `.html` files. It has no parent element.
- The only valid content are `<head>` and `<body>` children (in that order).
- `<!DOCTYPE html>` should preface the `<html>` opening tag.

The `<!DOCTYPE html>` statement _forces_ HTML5 interpretation mode for the document. It takes [guess work](https://developer.mozilla.org/en-US/docs/Web/HTML/Quirks_Mode_and_Standards_Mode) of the browser, and guarantees compatibility.

### `<head>` Metadata

- Allowed only once
- Machine-readable metadata
- [These](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head#see_also) elements are valid children.

### `<body>` Content

- Allowed only once
- Holds the entire visible viewport, all Elements that are not "Meta"
