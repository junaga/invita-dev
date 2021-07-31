# From Markdown to HTML

[HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) and [Markdown](https://commonmark.org/) are both so called [markup languages](https://en.wikipedia.org/wiki/Markup_language), used to create digital **documents**. HTML is more difficult, but also offers more capabilities. In combination with CSS and Javascript it is even used to build entire **applications** for the Web (the internet).

1. [Quick history](#Quick-history)
   1. [The HTML standard](#The-HTML-standard)
   2. [The fancy Markdown](#The-fancy-Markdown)
2. [Syntax differences](#Syntax-differences)
3. [Source samples](#Source-samples)

---

## Quick history

> “One of the things the Web teaches us is that everything is connected (hyperlinks) and we all should work together (standards). Too often school teaches us that everything is separate (many different ‘subjects’) and that we should all work alone.” -Aaron Swartz

### The HTML standard

HTML was created in 1993 with the very first Web Browser. After that, **many browsers**, with **many versions** of HTML and CSS followed.

1. Netscape
2. Internet Explorer (`-ms` in CSS)
3. Safari (`-webkit` in CSS)
4. Firefox (`-moz` in CSS)

In 2008 HTML has been unified, into HTML5 (`<!DOCTYPE html>`) the so called _Living standard_. But CSS remains different across browsers, everyone has their own _user agent stylesheet_. Making `<button>` look different on Firefox then chrome. A lot of browsers are not chromium based, (even though it's [open source](https://github.com/chromium/chromium)) creating headaches for web developers, and wasting companies time and money.

### The fancy Markdown

Invented in 2004. A simple perl script to transform a Markdown file `.md` into a `.html` one. It became a popular markup solution, because the source text itself also has good human readability. Since then, it took over the web pretty good. Web developers love to write their documentation in Markdown, and many blogs are built with it.

But common users are also in contact with Markdown here and there. A lot of Forums and Websites allow users to _markup_ their posts. A few quick example include:

- Reddit - posts
- StackOverflow - questions and answers
- GitHub - issues and comments

## Syntax differences

Markdown actually becomes transpiled into HTML during rendering. `## Title` becomes `<h2>Title</h2>`. For every Markdown statement there is an equivalent **element** in HTML.

While in Markdown there are multiple statements that declare a markup (There is the `#`, `##` headers syntax, the `1.` and `-` listing syntax). In HTML there is only a **single statement**, the **atomic element**. Elements are declared using the element name surrounded by angel brackets `<>`.

There are two types of elements

1. Normal elements `<NAME>CONTENT</NAME>`
2. Singleton elements `<NAME>`

Normal elements have an **opening tag** and a **closing tag** (notice the `/`). The **content** in between, are **other elements**. Singleton elements have no closing tag, and therefore cannot have other child elements as content. More on [MDN](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics).

Note: plain text itself, like `How are you?` is considered an element too in HTML.

## Source samples

This document itself "From Markdown to HTML" - `md2html.md` _is written_, in Markdown. To make sure you understand everything, you can check out its source text below. Following that, is a **HTML version** that shows how it could be written **using elements**.

Remember there are a lot of other HTML elements. Like `<button>` and `<video>` you can always check out other guides to learn about them.

```md

```

```html
Hello
```
