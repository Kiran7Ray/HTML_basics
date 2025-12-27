1.  \<!DOCTYPE html\> Theory: The \<!DOCTYPE html\> declaration is
    mandatory as the very first line in every HTML document. It
    instructs the browser to render the page in standards mode using
    HTML5 specifications, preventing quirks mode that could cause
    inconsistent rendering across browsers. Without it, browsers might
    fallback to legacy behaviors, leading to layout issues. This doctype
    is case-insensitive but conventionally written in lowercase. It's
    not an HTML tag but a document type declaration. GeeksforGeeks

Example:

xml

\<!DOCTYPE html\>

2.  ```{=html}
    <html>
    ```
    Element Theory: The

    ```{=html}
    <html>
    ```
    element serves as the root container for all other elements in the
    document, encapsulating the entire page structure. It must be the
    outermost wrapper after the doctype, with a closing

    ```{=html}
    </html>
    ```
    tag at the very end. Commonly includes the lang attribute (e.g.,
    lang="en") to specify the primary language, aiding screen readers,
    search engines, and translation tools for better accessibility and
    SEO. Additional attributes like xmlns can be used for XHTML
    compatibility, though rarely needed in HTML5. Always pair it with

    ```{=html}
    <head>
    ```
    and

    ```{=html}
    <body>
    ```
    children. WebPlatform

3.  ```{=html}
    <head>
    ```
    and Metadata Theory: The

    ```{=html}
    <head>
    ```
    element holds non-visible metadata about the document, such as
    title, character encoding, viewport settings, and SEO-related info.
    It never renders directly on the page but influences how browsers,
    search engines, and devices interpret the content. Key tags include:

```{=html}
<title>
```
: Sets the browser tab title and top search result text (keep under 60
characters for SEO).

```{=html}
<meta charset="UTF-8">
```
: Declares Unicode support for global characters, preventing garbled
text.

```{=html}
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
: Enables responsive design on mobiles by controlling zoom and scaling.

```{=html}
<meta name="keywords">
```
and
```{=html}
<meta name="description">
```
: Provide search engines with content summaries (though modern SEO
favors content over these).

```{=html}
<meta name="author">
```
: Credits the creator. Additional essentials: `<link rel="icon">`{=html}
for favicons, `<base>`{=html} for relative URLs, and
```{=html}
<script>
```
/
```{=html}
<style>
```
for deferred resources. Place
```{=html}
<head>
```
immediately after
```{=html}
<html>
```
.

Example:

xml

```{=html}
<head>
```
```{=html}
<meta charset="UTF-8">
```
```{=html}
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
```{=html}
<meta name="keywords" content="HTML, basics, web development">
```
```{=html}
<meta name="description" content="Learn core HTML elements.">
```
```{=html}
<meta name="author" content="Your Name">
```
```{=html}
<title>
```
HTML Basics
```{=html}
</title>
```
```{=html}
</head>
```
4.  ```{=html}
    <body>
    ```
    Element Theory: The

    ```{=html}
    <body>
    ```
    element encloses all user-facing, visible content on the webpage,
    including text, images, media, forms, and interactive elements. It
    starts right after

    ```{=html}
    </head>
    ```
    and ends before

    ```{=html}
    </html>
    ```
    . Browsers implicitly add a

    ```{=html}
    <body>
    ```
    if omitted, but explicit use is best practice for clarity and
    control. Supports global attributes like class, id, style, and event
    handlers (e.g., onload). In modern HTML5, it can include semantic
    children like

    ```{=html}
    <header>
    ```
    and

    ```{=html}
    <main>
    ```
    . Only one

    ```{=html}
    <body>
    ```
    per document; duplicate ones cause parsing errors.

5.  Headings (

    ```{=html}
    <h1>
    ```
    to

    ```{=html}
    <h6>
    ```
    ) Theory: Headings structure content hierarchically, signaling
    importance and sections to browsers, search engines, and assistive
    tech.

    ```{=html}
    <h1>
    ```
    denotes the highest-level heading (use only once per page for the
    main title), decreasing to

    ```{=html}
    <h6>
    ```
    for sub-subsections. They convey semantic meaning beyond
    size---search engines prioritize

    ```{=html}
    <h1>
    ```
    for SEO. Avoid skipping levels (e.g.,

    ```{=html}
    <h1>
    ```
    to

    ```{=html}
    <h3>
    ```
    ) for logical outline. Use with ARIA for accessibility if needed.
    Styling via CSS can override default bold/large appearance.

6.  Paragraphs (

    ```{=html}
    <p>
    ```
    ) Theory: The

    ```{=html}
    <p>
    ```
    tag defines semantic paragraphs, grouping related sentences into
    blocks with automatic top/bottom margins (typically 1em spacing).
    Browsers add line breaks and spacing, distinguishing it from
    `<br>`{=html} (line break only). Ideal for prose; nest other inline
    elements inside. Supports global attributes. Multiple consecutive

    ```{=html}
    <p>
    ```
    tags stack vertically. For non-paragraph blocks, use

    ```{=html}
    <div>
    ```
    instead to avoid unintended semantics.

7.  Text Formatting Tags Theory: These tags enhance text presentation
    and semantics:

`<strong>`{=html}: Indicates strong importance (renders bold; screen
readers emphasize tone).

`<b>`{=html}: Purely stylistic bold, no semantic weight.

`<em>`{=html}: Emphasizes stress (renders italic; screen readers alter
inflection).

`<i>`{=html}: Stylistic italics (e.g., for foreign words).

`<mark>`{=html}: Highlights text (yellow background by default) for
relevance.

```{=html}
<del>
```
: Strikethrough for deleted/removed content (with cite or datetime for
context).

```{=html}
<ins>
```
: Underline for inserted/added content (similar attributes). Prefer
semantic tags (`<strong>`{=html}, `<em>`{=html}) over visual ones for
accessibility and SEO. Can nest and combine.

8.  Links (`<a>`{=html}) Theory: The anchor `<a>`{=html} creates
    hyperlinks for navigation using href (URL or anchor target).
    Additional attributes: target="\_blank" for new tabs, rel="noopener"
    for security, title for tooltips, download for files. Internal links
    use relative paths (e.g., href="#section" for page jumps). Makes
    text/images clickable. Semantic for navigation; avoid for styling
    buttons (use `<button>`{=html}). Validate URLs to prevent broken
    links.

Example:

xml
`<a href="https://example.com" target="_blank" rel="noopener">`{=html}Visit
Example`</a>`{=html} 9. Images (`<img>`{=html}) Theory: The
`<img>`{=html} tag embeds images without a closing tag (void element).
Requires src for source path/URL and alt for accessibility (screen
reader description; empty for decorative). Enhancers: width/height for
dimensions (use CSS for responsiveness), loading="lazy" for performance,
srcset/sizes for responsive images. Supports formats like WebP for
optimization. Fallback via `<picture>`{=html} for art direction.

10. Lists Theory: Lists organize data semantically.

Unordered (
```{=html}
<ul>
```
): Bulleted items via
```{=html}
<li>
```
for non-sequential sets (e.g., shopping lists).

Ordered (
```{=html}
<ol>
```
): Numbered via
```{=html}
<li>
```
with reversed or start attributes for sequences (e.g., steps). Nest
lists inside
```{=html}
<li>
```
for hierarchies. Use
```{=html}
<dl>
```
,
```{=html}
<dt>
```
,
```{=html}
<dd>
```
for descriptions. CSS customizes bullets/numbers.

Example:

xml

```{=html}
<ul>
```
```{=html}
<li>
```
Item 1
```{=html}
</li>
```
```{=html}
<li>
```
Item 2
```{=html}
</li>
```
```{=html}
</ul>
```
```{=html}
<ol>
```
```{=html}
<li>
```
Step 1
```{=html}
</li>
```
```{=html}
<li>
```
Step 2
```{=html}
</li>
```
```{=html}
</ol>
```
11. Tables (

    ```{=html}
    <table>
    ```
    ) Theory: Tables present tabular data with

    ```{=html}
    <table>
    ```
    as container,

    ```{=html}
    <tr>
    ```
    for rows,

    ```{=html}
    <th>
    ```
    for headers (scope attributes for accessibility),

    ```{=html}
    <td>
    ```
    for cells. Structure with

    ```{=html}
    <thead>
    ```
    ,

    ```{=html}
    <tbody>
    ```
    ,

    ```{=html}
    <tfoot>
    ```
    for sections. Attributes: colspan/rowspan for merging. Use
    role="table" for ARIA if semantic issues. Caption via

    ```{=html}
    <caption>
    ```
    . Avoid for layout (use CSS Grid/Flexbox).

12. ```{=html}
    <iframe>
    ```
    Theory: Embeds external content (e.g., videos, maps) via src URL.
    Attributes: width/height, sandbox for security restrictions,
    allowfullscreen, loading="lazy". Same-origin policy limits
    interactions. Responsive via CSS. Use srcdoc for inline HTML.
    Alternatives: `<object>`{=html} or `<embed>`{=html} for broader
    support.

13. Audio & Video (`<audio>`{=html} & `<video>`{=html}) Theory: Native
    HTML5 multimedia without plugins. `<audio>`{=html} for sound (src or
    `<source>`{=html} tracks with type); `<video>`{=html} for clips (add
    poster for thumbnail). controls adds player UI; autoplay/loop/muted
    for behavior (autoplay restricted). Multiple `<source>`{=html} for
    fallbacks (e.g., MP4/WebM). preload manages loading. Subtitles via
    `<track>`{=html}.

14. Forms (

    ```{=html}
    <form>
    ```
    ) and Inputs Theory:

    ```{=html}
    <form>
    ```
    collects/submits data via action (server endpoint) and method
    ("GET"/"POST"). Inputs:
    `<input type="text|email|password|number|checkbox|radio|file|submit">`{=html},

    ```{=html}
    <textarea>
    ```
    for multiline, `<select>`{=html} with
    `<option>`{=html}/`<optgroup>`{=html}, `<button>`{=html} types.
    Labels via `<label for="id">`{=html}. Validation: required, pattern,
    min/max. Accessibility with ARIA.

15. Semantic Layout Tags Theory: HTML5 semantics improve
    structure/SEO/accessibility:

```{=html}
<header>
```
: Page/banner or section intro.

```{=html}
<nav>
```
: Main navigation.

```{=html}
<main>
```
: Primary content (one per page).

```{=html}
<section>
```
: Themed groupings with headings.

```{=html}
<article>
```
: Standalone, reusable content (e.g., blog post).

```{=html}
<aside>
```
: Sidebar/pull-quote.

```{=html}
<footer>
```
: Closing info (page or section). Combine with
```{=html}
<div>
```
for non-semantic containers. Outline algorithm aids screen readers.

16. CSS (Cascading Style Sheets) Theory: CSS styles HTML for
    visuals/layout. Methods:

Internal:
```{=html}
<style>
```
in
```{=html}
<head>
```
.

External: `<link rel="stylesheet" href="styles.css">`{=html}.

Inline: style attribute (avoid for maintainability). Selectors target
elements (e.g., body { background: lightblue; color: navy; font-family:
Arial; }). Covers colors, fonts, spacing, Flexbox/Grid for layout,
animations, responsive @media queries. Cascade resolves conflicts by
specificity/order. Preprocessors like Sass extend it.

Example:

xml

```{=html}
<style>
  body { background: lightblue; font-family: Arial, sans-serif; margin: 20px; }
  h1 { color: navy; }
</style>
```
17. Div and Span (Container Elements) Theory:
    ```{=html}
    <div>
    ```
    creates block-level divisions for grouping/layout (no semantic
    meaning). `<span>`{=html} is inline for styling text snippets. Both
    hook CSS/JS via class/id. Essential for non-semantic containers
    before Flexbox/Grid.

Example:

xml

::: container
[Highlighted]{style="color: red;"}
:::

18. Comments and Global Attributes Theory: `<!-- Comment -->`{=html}
    hides notes from rendering (nestable). Global attributes (e.g., id,
    class, style, title, data-\* for custom, hidden, tabindex) apply to
    most elements for ID targeting, styling, accessibility, and
    extensibility.
