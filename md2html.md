# From Markdown to HTML

[Markdown](https://commonmark.org/) and [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) are both so called [markup languages](https://en.wikipedia.org/wiki/Markup_language), used to create digital **documents**. Under the hood, Markdown actually _becomes_ HTML when displayed. So any Markdown document can also be written in HTML directly. HTML is more difficult, but also offers more capabilities. In combination with CSS and Javascript it can even be used to build entire **applications** for the Web (the internet).

1. [Quick history](#quick-history)
   1. [The HTML standard](#the-html-standard)
   2. [The fancy Markdown](#the-fancy-markdown)
2. [Syntax differences](#syntax-differences)
3. [Transpilation example](#transpilation-example)

---

## Quick history

> "One of the things the Web teaches us is that everything is connected (hyperlinks) and we all should work together (standards). Too often school teaches us that everything is separate (many different 'subjects') and that we should all work alone." -Aaron Swartz

### The HTML standard

HTML was created in 1993 with the very first Web Browser. After that, **many browsers**, with **many versions** of HTML and CSS followed.

1. Netscape
2. Internet Explorer (`-ms` in CSS)
3. Safari (`-webkit` in CSS)
4. Firefox (`-moz` in CSS)

In 2008 HTML has been unified, into HTML5 (`<!DOCTYPE html>`) the so called _Living standard_. But CSS remains different across browsers, everyone has their own _user agent stylesheet_. Making `<button>` look different on Firefox then Chrome.

### The fancy Markdown

Invented in 2004. A simple perl script to transform a Markdown file `.md` into a `.html` one. It became a popular markup solution, because the source text itself also has good readability. Since then, it took over the web pretty good. Web developers love to write their documentation in Markdown, and many blogs are built with it.

But common users also come frequently in contact with Markdown. A lot of Forums and Websites allow users to _markup_ their posts. A few quick example include:

- Reddit - posts
- StackOverflow - questions and answers
- GitHub - issues and comments

## Syntax differences

Markdown _becomes transpiled_ into HTML, which in turn then renders, the actual view. `## Title` becomes `<h2>Title</h2>`. For every Markdown statement, there is an equivalent **element** in HTML. While in Markdown, there are multiple statements that declare a markup (There is the `#` and `##` headers syntax. The `1.` and `-` listing syntax). There is only a single statement in HTML, the HTML **element**.

Elements are declared using the **element name** surrounded by **angel brackets** `<`, `>`. They can optionally include HTML **attributes**. There are two types of elements:

1. Normal elements: `<ELEMENT ATTRIBUTE="VALUE" ...>CONTENT</ELEMENT>`
2. Singleton elements: `<ELEMENT ATTRIBUTE="VALUE" ...>`

Attributes **are optional** and are always written in the **opening tag**, seperated by a blank space. Normal elements have an opening tag and a **closing tag** (notice the `/`). The **content** in between, are **other elements** recursively nested. Singleton elements have no closing tag, and therefore cannot have other child elements as content. More on [MDN](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics).

Note: Plain text itself, like `How are you?` is considered an element too in HTML.

## Transpilation example

Here is a quick example of how Markdown becomes HTML. Take a look at the Markdown file below. It consists of a heading (a title), some paragraphs, an item list, and bold and italic text emphasis. Following that, comes its transpiled HTML output. The HTML output includes these elements:

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

### The transpiled HTML output

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

Note: Whitespace (Newline, Space etc), is actually ignored in HTML. This code includes line breakes only to improve readibly for the author. This is done automaticly by code formatting tools like [prettier](https://prettier.io/). The entire HTML could just as well be written in a single line.

Note: This HTML is a slightly simplified version of the actual transpiled output. The `id` attribute was dropped, and `<strong>` and `<em>` were replaced by `<b>` and `<i>`. Both versions are equal to the reader, they produce the exact same view (semantically and stylistically) when rendered.
