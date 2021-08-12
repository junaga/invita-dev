# Von Markdown zu HTML

[Markdown (vereinfachte Auszeichnungssprache)](https://commonmark.org/) und [HTML](https://developer.mozilla.org/de/docs/Web/HTML) sind beide sogenannte [Markup Sprachen (Auszeichnungssprachen)](https://de.wikipedia.org/wiki/Auszeichnungssprache), die verwendet werden, um digitale **Dokumente** zu erstellen. Tatsächlich _wird_ Markdown zu HTML, wenn es angezeigt wird. Das heißt, jedes Markdown-Dokument kann auch direkt in HTML geschrieben werden. HTML ist komplizierter, bietet aber auch mehr Möglichkeiten. In Kombination mit CSS und Javascript, kann es sogar genutzt werden, um ganze **Anwendungen** für das Web (das Internet) zu erstellen.

1. [Schnelle Geschichte](#schnelle-geschichte)
   1. [Der HTML Standard](#der-html-standard)
   2. [Das schicke Markdown](#das-schicke-markdown)
2. [Syntax Unterschiede](#syntax-unterschiede)
3. [Transpilationsbeispiel](#transpilationsbeispiel)
4. [Lernen durch Handeln](#lernen-durch-handeln)

---

## Schnelle Geschichte

> "Eines der Dinge, die das Internet lehrt, ist, dass alles verbunden ist (Hyperlinks) und wir sollten alle zusammenarbeiten (Standards). Zu oft lehrt uns die Schule, dass alles getrennt ist (viele verschiedene "Themen") und,dass wir alle alleine arbeiten sollten." -Aaron Swartz

### Der HTML Standard

HTML wurde im Jahr 1993 mit dem ersten Webbrowser entwickelt. Danach folgten **viele Browser** mit **vielen Versionen** von HTML und CSS.

1. Netscape
2. Internet Explorer (`-ms` in CSS)
3. Safari (`-webkit` in CSS)
4. Firefox (`-moz` in CSS)

Im Jahr 2008 wurde HTML einheitlich in HTML5 (`<! Doctype html>`), den sogenannten _LIVE-Standard_, übernommen.
CSS bleibt jedoch zwischen den Browsern unterschiedlich, jeder verfügt über ein eigenes _user-Agent-Stylesheet_.
Das hat zur Folge, dass `<Knöpfe>` in Firefox anders aussehen, als in Chrome.

### Das schicke Markdown

Im Jahr 2004 erfunden. Ein einfaches Perl-Skript, um eine Markdown-Datei `.md` in eine `.html` zu wandeln.
Es wurde zu einer beliebten Markup-Lösung, da auch der Quelltext selbst eine gute Lesbarkeit hat. Seitdem wurde es vom Web ziemlich gut angenommen. Web-Entwickler lieben es, ihre Dokumentation in Markdown zu schreiben, und viele Blogs werden damit gebaut.

Normale Benutzer kommen jedoch auch häufig in Kontakt mit Markdown. Viele Foren und Websites ermöglichen Benutzern ihre Beiträge zu _MarkUp_-en. Ein paar schnelle Beispiele umfassen:

- Reddit -Posts
- StackOverflow - Fragen und Antworten
- GitHub - Probleme und Kommentare

## Syntax Unterschiede

Markdown wird zu HTML _transpiliert_, was wiederum die tatsächliche Ansicht rendert. `## Titel` wird `<h2>Titel</h2>`. Für jede Markdown-Anweisung gibt es ein Äquivalent **Element** in HTML. Während es in Markdown mehrere Anweisungen gibt, die ein MarkUp deklarieren (Es gibt das `#` und `##` Überschrift-Syntax. Das `1.` und `-` Auflistung-Syntax), gibt es nur eine einzige Anweisung in HTML, das HTML **Element**.

Elemente werden mit dem **Elementnamen**, der von **Engel-Klammern** umgeben ist, deklariert `<`, `>`. Sie können optional HTML **Attribute** enthalten. Es gibt zwei Arten von Elementen:

1. Normale Elemente: `<ELEMENT ATTRIBUT="WERT" ...>INHALT</ELEMENT>`
2. Singleton Elemente: `<ELEMENT ATTRIBUT="WERT" ...>`

Attribute **sind optional** und werden immer in den **öffnende Tag (Marker)** geschrieben, der von einem Leerzeichen getrennt wird. Normale Elemente verfügen über einen Öffnungs-Tag und einen **Schließen-Tag** (Zu beachten sind die `/`). Der **Inhalt** dazwischen sind **andere Elemente**, rekursiv verschachtelt. Singleton-Elemente haben keinen Schließungs-Tag und können daher keine anderen untergeordneten Elemente als Inhalt haben. Mehr auf
[MDN](https://developer.mozilla.org/de/docs/Learn/Getting_started_with_the_web/HTML_basics).

Hinweis: Einfacher Text, wie `Wie geht es Ihnen?` Wird auch als Element in HTML betrachtet.

## Transpilationsbeispiel

Hier ist ein kurzes Beispiel dafür, wie Markdown zu HTML wird. Man betrachte die untenstehende Markdown-Datei. Sie besteht aus einer Überschrift (einem Titel), einigen Absätzen, einer Inhaltsliste und einem fetten und kursiven Text.Danach kommt die transpilierte HTML-Ausgabe. Die HTML-Ausgabe enthält diese Elemente:

- `<p>` - Paragraph
- `<h2>` - Überschrift
- `<ul>` und `<li>` - Unsodtierte Liste und Listeninhalten
- `<a>` mit `href` - Anker mit Hypertext-Referenz
- `<b>` - Fett gedruckt
- `<i>` - Kursiv

Um mehr über diese Elemente zu erfahren, bietet sich das MDN an [HTML-Elemente-Referenz](https://developer.mozilla.org/de/docs/Web/HTML/Element).

### Der Markdown-Quelltext

```md
## Die Gutenberg Presse

Die [Druckpresse](https://de.wikipedia.org/wiki/Druckpresse) wurde vom Goldschmied Johannes Gutenberg erfunden.
Die Gutenbergpresse war eine dramatische Verbesserung im Vergleich zu früheren Druckmethoden. Sie wird als die **wichtigste** Erfindung des zweiten Milleniums bezeichnet.

- In Deutschland um 1440 erfunden
- Beinhaltete _bewegliche_ Glyhpen
- Konnte bis zu 3.600 Seiten pro Arbeitstag produzieren

Der Betrieb einer Druckerpresse wurde Synonym für das Druckgeschäft.
Sie ist ebenso namensgebend für die neuste Kommunikationsform der Gesellschaft "Die Presse".
Journalismus wurde geboren.

Es ist leicht zu behaupten, dass das 90er-Web (das Internet) eine neue Iteration von derselben Erfindung ist. Es hat es beidem einfacher gemacht: Information zu veröffentlichen _und_ zu konsumieren. Die menschliche Kommunikation fand beinahe in Echtzeit statt und näherte sich der Lichtgeschwindigkeit.
```

### Die transpilierte HTML-Ausgabe

```html
<h2>Die Gutenberg Presse</h2>
<p>
  Die <a href="https://de.wikipedia.org/wiki/Druckpresse">Druckpresse</a> wurde
  vom Goldschmied Johannes Gutenberg erfunden. Die Gutenbergpresse war eine
  dramatische Verbesserung im Vergleich zu früheren Druckmethoden. Sie wird als
  die <b>wichtigste</b> Erfindung des zweiten Milleniums bezeichnet.
</p>
<ul>
  <li>In Deutschland um 1440 erfunden</li>
  <li>Beinhaltete <i>bewegliche</i> Glyphen</li>
  <li>Konnte bis zu 3.600 Seiten pro Arbeitstag produzieren</li>
</ul>
<p>
  Der Betrieb einer Druckerpresse wurde Synonym für das Druckgeschäft. Sie ist
  ebenso namensgebend für die neuste Kommunikationsform der Gesellschaft "Die
  Presse". Journalismus wurde geboren.
</p>
<p>
  Es ist leicht zu behaupten, dass das 90er-Web (das Internet) eine neue
  Iteration von derselben Erfindung ist. Es hat es beidem einfacher gemacht:
  Information zu veröffentlichen
  <i>und</i> zu konsumieren. Die menschliche Kommunikation fand beinahe in
  Echtzeit statt und näherte sich der Lichtgeschwindigkeit.
</p>
```

Hinweis: Whitespaces (Zeilenumbrüche, Leerzeichen usw.), werden normalerweise in HTML ignoriert. Dieser Code enthält Linienbrüche, die nur für den Autor vorgesehen sind. Dies erfolgt automatisch von Code-Formatierungswerkzeugen wie [prettier](https://prettier.io/). Das gesamte HTML könnte genauso gut in einer einzigen Zeile geschrieben werden.

Hinweis: Dieses HTML ist eine etwas vereinfachte Version der tatsächlichen transpilierten Ausgabe. Das `id` Attribut wurde entfernt und `<strong>` und `<em>` wurden durch ersetzt durch `<b>` und `<i>`. Beide Versionen sind für den Leser identisch, sie erzeugen die genaue Ansicht (semantisch und stilistisch), wenn sie gerendert werden.

## Lernen durch Handeln

Ich ermutige jeden, einfach etwas HTML zu schreiben, um den Umgang damit zu lernen. Einfach ein paar HTML-Dateien im Browser öffnen und mit[DevTools](https://developer.chrome.com/docs/devtools/) (`strg+shift+j`) überprüfen. Wenn man sich noch nicht bereit fühlt, ist [MDN](https://developer.mozilla.org/de/) ist der beste Ort, um mehr über das Internet zu lernen.
