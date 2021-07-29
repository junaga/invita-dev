My own (strongly opinionated) HTML reference of **elements** and **attributes**. Built using personal experience, the [MDN ref](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference) and the [AMPHTML spec](https://github.com/ampproject/amphtml/blob/main/docs/spec/amp-html-format.md). Grouped by three sections:

1. [Head and misc](#head-and-misc). **Not visible** elements, including weird things like comments.
2. [Body](#Body). **Real elements**, to be used inside `<body>`.
3. [Global Attributes](#Global-Attributes). All elements, including the top level `<html>` root, **can have** these attributes.

I only consider `.html` files _production grade_, if they follow the conventions listed here.

# Head and misc

Comments `<!-- -->` can be used **anywhere**. Conditional comments are not allowed.

There can only be one `<html>`, `<head>` and `<body>` element per `.html` file.

### `<html>` Document

The top level element, all other elements are children of it. The `<!DOCTYPE html>` preamble should be put in front its opening tag, to force HTML5 for the document. That way we take [guess work](https://developer.mozilla.org/en-US/docs/Web/HTML/Quirks_Mode_and_Standards_Mode) of the browser, and guarantee compatibility.

# Body

## Whitelist

#### `<div>` Division

A generel purpose element or container. If there exists a semantically more meaningfull element. For the love of god, use it.

### Text content elements

#### `<p>` Paragraph

- simple, line wrapped text
- exists in Markdown (has no statement/operator)

### Text Elements

The `<p>` Paragraph, is a simple wrapped text line. I consider it the most basic Element.

Inside `<p>`, `<b>` or `<i>` can be used to annotate indivual words.
