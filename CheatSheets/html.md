# HTML Cheat Sheet

## General Elements
* `<!DOCTYPE html>`
  * Declares the document to be an HTML document.
* `<html>`
  * Top-most Element.
* `<body>`
  * Container for all visible content.
* `<head>`
  * Container for all document metadata.
* `<a>`
  * Defines a link to another page or part of a page.
  * `href` attribute to contain the url of the link.
    * Use `#` to reference an ID on a page: `<a href="#footer">Go to footer</a>`
  * Use `mailto:` at the start of `href` string to cause the link to send an email.
    * `<a href="mailto:tim@email.com">Email Tim</a>` 
  * `target="_blank"` to open link in new tab.

## Head Elements 
* `<title>`
  * Title of document.
* `<meta>`
  * Document metadata.
* `<script>`
  * Include external or contain embedded JavaScript.
* `<link>`
  * Mainly used to include CSS files, but also used for favicons and fonts.
* `<style>`
  * Embedded CSS.
* `<base>`
  * Specifies a base URL for the document.

## Text Elements
* `<p>`
  * Defines a paragraph.
* `<b>`
  * Makes text bold.
  * No semantic meaning.
* `<i>`
  * Makes text italic.
  * No semantic meaning.
* `<sup>`
  * Superscript text: 1<sup>st</sup>
* `<sub>`
  * Subscript text: CO<sub>2</sub>
* `<br>`
  * Line break. Typically within a paragraph.
  * Self-closing.
* `<hr>`
  * Horizontal rule: a line across the document.
  * Self-closing.
  * Can act as a separator between content.

## Semantic Elements
* `<h1> to <h6>`
  * Structurally semantic headers.
* `<strong>`
  * Makes text bold.
  * Indicates strong importance.
* `<em>`
  * Makes text italic.
  * Indicates emphasis that subtly changes the meaning of the sentence.
* `<blockquote>`
  * For long quotes that take up an entire paragraph.
* `<q>`
  * For shorter quotes that sit within a paragraph.
* `<abbr>`
  * Defines an abbreviation.
  * Title attribute is used to specify the full term.
* `<cite>`
  * Indicates the title of a piece of work you are referencing such as a book, film, paper etc.
  * Not used on the creator's name, just the title of the work.
* `<dfn>`
  * Indicates the first instance of some new terminology.
* `<address>`
  * Contains the contact details of the author of the page.
* `<del>`
  * Strikes through text to denote a deletion.
* `<ins>`
  * Underlines text to denote an insertion.
* `<s>`
  * Indicates with a strike-through that something is no longer accurate or relevant but should not be deleted.

## List Elements
* `<ol>`
  * Container for an ordered list.
* `<ul>`
  * Container for an unordered list.
* `<li>`
  * List item for either a `<ol>` or `<ul>`.
* `<dl>`
  * Container for a definition list.
* `<dt>`
  * The term being defined within a `<dl>`.
* `<dd>`
  * The definition of the `<dt>` within a `<dl>`.

## Image Elements
* `<img>`
  * Self-closing.
  * Inline element.
  * Must use *at least* `src` and `alt` attributes.
  * `src` attribute defines the URL of the image.
  * `alt` provides a textual description of the image if you cannot see it.
  * `title` often used to provide additional information.
  * Using `height` and `width` attributes can allow a slow loading browser to render the rest of the page whilst leaving room for the images.