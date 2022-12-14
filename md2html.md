# From Markdown to HTML

[Markdown][] and [HTML][] are both so called [markup languages][], used to author (declaratively) digital **documents**. [Learn Markdown in 60 seconds](https://commonmark.org/help/).

[markdown]: https://daringfireball.net/projects/markdown/syntax
[html]: https://developer.mozilla.org/en-US/docs/Web/HTML
[markup languages]: https://en.wikipedia.org/wiki/Markup_language

Under the hood, Markdown actually _becomes_ HTML when displayed. So any Markdown document can also be written in HTML directly. HTML is more difficult, but also offers more capabilities. In combination with CSS and Javascript it can even be used to build entire **applications** for the Web (the internet).

1. [The fancy Markdown](#the-fancy-markdown)
2. [The HTML standard](#the-html-standard)
3. [Syntax differences](#syntax-differences)
4. [Transpilation example](#transpilation-example)

> "One of the things the Web teaches us is that everything is connected (hyperlinks) and we all should work together (standards). Too often school teaches us that everything is separate (many different 'subjects') and that we should all work alone."

\- Aaron Swartz

## The fancy Markdown

Invented in 2004. A simple perl script to transform a Markdown file `.md` into a `.html` one.

It became a popular markup language, because the source text itself also has good readability. Since then, it took over the web pretty good. Web developers love to write their documentation in Markdown, and many websites _like blogs_ are built with it.

### Where Markdown works

Common users also come into contact with Markdown and its "flavours". A lot of Forums and Apps allow users to _markup_ their posts. Examples include:

- Reddit
- StackOverflow
- GitHub
- Discord
- WhatsApp

## The HTML standard

HTML was created in 1990 (first spec 1993) with the very first Web Browser. After that, [many browsers](https://upload.wikimedia.org/wikipedia/commons/7/74/Timeline_of_web_browsers.svg), with many versions of HTML and CSS followed.

1. Netscape
2. Internet Explorer `-ms-`
3. Firefox `-moz-`
4. Safari `-webkit-`
5. Chrome `-webkit-`

> WebCore from Webkit from Safari, was forked into Blink for Chromium for Chrome

In 2008 HTML has been replaced (by the [WHATWG](https://whatwg.org/)) with HTML5 `<!DOCTYPE html>`, the so called _Living standard_. But CSS remains different across browsers, and everyone has their own _user agent stylesheet_. Making `<button>` look different on Firefox than Chrome.

## Syntax differences

Markdown _becomes transpiled_ into HTML, which then renders into the actual view. For every Markdown statement, there is an equivalent **element** in HTML. `## Title`, becomes `<h2>Title</h2>`. There are multiple types of elements in HTML:

1. Text nodes: `Have a nice day`
2. Elements: `<ELEMENT ATTRIBUTE="VALUE" ...>CONTENT</ELEMENT>`
   1. Void Elements: `<ELEMENT ATTRIBUTE="VALUE" .../>`
3. Comments: `<!-- -->`

> Plain text and comments, are **not actually** elements, they are DOM nodes.

HTML Elements are declared using the element name surrounded by angel brackets `<`, `>`.

- While in Markdown, there are multiple statements that declare a markup (There is the `#` and `##` headers syntax. The `1.` and `-` listing syntax). There is only a single statement in HTML, the HTML element.
- Normal elements have an opening tag and a closing tag (notice the `/`). The **content** in between, are other elements recursively nested. Void elements have no closing tag, and cannot have other child elements as content.
- **Attributes** are optional, and are always written in the opening tag seperated by a blank space.

More on [web.dev/learn/html](https://web.dev/learn/html)

## Transpilation example

Here is a quick example of how Markdown becomes HTML. Take a look at the Markdown block below. It consists of a heading (a title), some paragraphs, an item list, and bold and italic text emphasis. Following that, comes its transpiled HTML output. The HTML output includes these elements:

- `<p>` - Paragraph
- `<h2>` - Heading
- `<ul>` and `<li>` - Unordered list and List item
- `<a>` with `href` - Anchor with Hypertext reference
- `<b>` - Bold
- `<i>` - Italic

To learn more about these elements, you can checkout the MDN [HTML elements reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

### The Markdown source text

```md
## The Gutenburg Press

The [printing press](https://wikipedia.org/wiki/Printing_press) was
invented by goldsmith Johannes Gutenberg. The Gutenberg press was a dramatic
improvement compared to previous printing methods. It is credited with being
the **most significant** invetion, of the second millennium.

- Invented around 1440 in Germany
- Included a mould of _movable_ glyhps
- Could produce up to 3,600 pages per workday

The operation of a press became synonymous with the business of printing. It
also gave name to societies newest form of communication "the press".
Journalism was born.

It is easy to argue that the 90's web (the internet), is a new iteration of
that very same invention. It made it easier to both: publish
_and_ consume information. Human communication became almost instant,
closing in on the speed of light.
```

### The transpiled HTML

```html
<h2>The Gutenburg Press</h2>
<p>
  The <a href="https://wikipedia.org/wiki/Printing_press">printing press</a> was
  invented by goldsmith Johannes Gutenberg. The Gutenberg press was a dramatic
  improvement compared to previous printing methods. It is credited with being
  the <b>most significant</b> invetion, of the second millennium.
</p>
<ul>
  <li>Invented around 1440 in Germany</li>
  <li>Included a mould of <i>movable</i> glyhps</li>
  <li>Could produce up to 3,600 pages per workday</li>
</ul>
<p>
  The operation of a press became synonymous with the business of printing. It
  also gave name to societies newest form of communication "the press".
  Journalism was born.
</p>
<p>
  It is easy to argue that the 90's web (the internet), is a new iteration of
  that very same invention. It made it easier to both: publish
  <i>and</i> consume information. Human communication became almost instant,
  closing in on the speed of light.
</p>
```

> Whitespace (Newline, Space etc), is actually ignored in HTML. This code includes line breakes only to improve readibly for the author. This is done automaticly by code formatting tools like [prettier](https://prettier.io/). The entire HTML could just as well be written in a single line.

> This HTML is a slightly simplified version of the actual transpiled output. The `id` attribute was dropped, and `<strong>` and `<em>` were replaced by `<b>` and `<i>`. Both versions are equal to the reader, they produce the exact same view (semantically and stylistically) when rendered.

### The Rendered Document

---

## The Gutenburg Press

The [printing press](https://wikipedia.org/wiki/Printing_press) was
invented by goldsmith Johannes Gutenberg. The Gutenberg press was a dramatic
improvement compared to previous printing methods. It is credited with being
the **most significant** invetion, of the second millennium.

- Invented around 1440 in Germany
- Included a mould of _movable_ glyhps
- Could produce up to 3,600 pages per workday

The operation of a press became synonymous with the business of printing. It
also gave name to societies newest form of communication "the press".
Journalism was born.

It is easy to argue that the 90's web (the internet), is a new iteration of
that very same invention. It made it easier to both: publish
_and_ consume information. Human communication became almost instant,
closing in on the speed of light.

---

> Depending on additional CSS the rendered document looks different. Unfortunatly every Browser has a different CSS default, called the [user agent stylesheet](https://web.dev/learn/css/box-model/#user-agent-stylesheets).

> To enforce consistency add some custom CSS (like a [CSS reset](https://github.com/search?q=css+reset)) to your document. Another solution would be to just use Google Chrome or Microsoft Edge, and insult everyone (including your users) with a different browser. (thats what I do)
