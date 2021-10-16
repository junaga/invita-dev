# Markdown - `.md`

Invented in 2004, **Mark-_down_** is a [mark-_up_ language](https://en.wikipedia.org/wiki/Markup_language), used to create [hypertext](https://en.wikipedia.org/wiki/Hypertext) [documents](https://en.wikipedia.org/wiki/Writing). It is used accross [the web](https://en.wikipedia.org/wiki/World_Wide_Web) by both, **devs** and **users** alike.

## Why Markdown

It is simple, readable and widly adopted. Markdown is the most commonly used _lightweight_ markup language.

- A lot of content centric **websites**, like blogs and technical docs, are build from `.md` files.
- Web developers know and love Markdown. They use it to write **software documentation**, like README and CONTRIBUTING files, or API overviews.
- **Posts** and **comments** in some apps are Markdown(-based), including
  - GitHub
  - Reddit
  - Stack Exchange, Stack Overflow

Different from a "What you see is what you get" document editing application like Microsoft Word. A Markdown document is simply a **text file** (usually UTF-8 encoded) ending in `.md`. The writen source needs to be renderd into a **preview** using an appropriate application.

## Getting started

You can use the [VS Code](https://code.visualstudio.com/) editor, simply click the [preview button][vscode-md-preview] to see your markdown source rendered.

### Advanced

Alternativly You could also use an online tool, or manually convert your Markdown to HTML. Make sure to format your Markdown source with prettier to guarentee

## Elements

You can markup words, phrases or paragraphs within Markdown using _any combination_ of the following elements.

### `_Italic_`

Surround some text with `_` underscores to emphasize it. For "_This is_ emphasized text" do `_This is_ emphasized text`.

1. Foreign words, technical Terms, Taxonomic designations, etc.

   - The Latin phrase _Veni, vidi, vici_ is often mentioned in music, art, and literature.
   - A _Markup language_ is a computer language used to create digital documents.
   - _Homo sapiens_ are the most abundant and widespread species of primate, characterized by bipedality, large and complex brains enabling the development of advanced tools, culture and language.

2. Stressed pronounciation. If something is spoken in a different tone. (in HTML this can be done with `<em>`)

   - I _didn't_ take the test yesterday. (I did not take it.)
   - I didn't _take_ the test yesterday. (I did something else with it.)
   - I didn't take the test _yesterday_. (I took it some other day.)

### `**Bold**`

Surround some text with `**` two asterisks to highlight it. For "This is a highlighted **keyword**" do `This is a highlighted **keyword**`.

Within a larger body of text, a piece in _italics_ does not stand out much. Instead, it signifies a context difference only _while_ the text is being read. By contrast, a single **bold** word attracts the human eyeball and is therefore recommended for keywords the reader might be _looking_ for.

### `## Heading`

[vscode-md-preview]: https://code.visualstudio.com/docs/languages/markdown#_dynamic-previews-and-preview-locking
