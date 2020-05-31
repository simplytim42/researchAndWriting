# `<head>`

>Last Updated: 31-05-2020

The `head` tag contains metadata about the HTML document. All of its content is contained within other tags.

## `<title>`
* Supplies the browser tab with text.
* Provides the default name if page is bookmarked.

## `<meta>`

* Self-closing.
* Supplies metadata (SHOCK HORROR!).
* Each `meta` provides a single data point using a name/value pair using two element attributes.
* The `name` attribute provides document-level metadata and must be combined with the `content` attribute.
	* "author", "application-name" and "keywords" don't seem to be used much anymore.
	* "description" used in google search results. More than 160 characters may not show on search engine results.
	* "viewport" used in responsive web design. If site is not responsive, this could make it worse.
	* "robots" dictates how search engines should react to this page.
* The `http-equiv` attributes simulate HTTP response headers: short for http-equivelant.
	* "content-type" is the character encoding declaration and is usually shortened down to `<meta charset="utf-8">`.
	* "refresh" refreshes the page after x seconds and can optionally redirect.

## `<script>`
* `type` attribute not needed anymore, was required in html4.
* Javascript can be put inbetween `script` tags but its more DRY to link to separate file using the `src` attribute.
* Each JS file being loaded requires its own `script` tag.
* By default, HTML doc loading is halted to load JS.
	* `async` or `defer` attributes can alter this.
	* Use `defer` if the JS being loaded references the DOM.

## `<link>`
* Self-closing.
* Loads external resources, mainly CSS but can be any other resources such as favicons and fonts.
	* `href` and `rel` attributes must always be used.
	* `href` defines the address of the resource.
	* `rel` defines the relationship of the resource: stylesheet, icon etc.
	* `type` is assumed by default to be "text/css" so only specify `type` when is isn't "text/css".

## `<style>`
* Similar to `<script>` in the sense that it contains code> specifically CSS code.
* Unlike `<script>` you cannot reference external stylesheets, that must be done using `<link>`.
* The `media` attribute provides conditions for the contained CSS.
	* Original use case was formatting for print.
	* These days used for Responsive Design.
* Usually put in the `<head>`.

## `<base>`
* Self-closing.
* Main purpose is to specify the Base URL for the document.
	* This means **all** relative URLs in the document will be based off the `base` value.
	* Unless you have a very deep and complicated directory hierarchy this probably won't be needed.
## Typical `<head>` Heirarchy
```html
<head>
	<base>
	<meta>
	<title>Simply Tim's Page</title>
	<link>
	<style>
		Embedded CSS
	</style>
</head>
```
