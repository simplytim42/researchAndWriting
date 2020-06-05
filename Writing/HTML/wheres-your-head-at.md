# Where's Your `<head>` At?

>DATE HERE

The `<head>` tag is easily overlooked. Primarily concerned with the document's metadata, there is an awful lot that can potentially go inside the `<head>`, but not so much that probably *will*. This article takes a look at the more common subordinates of the `<head>` tag.

---

## `<title>`
The simplest of all the `<head>` elements, `<title>` is the 'title' of the HTML document. You want try and make this unique to each page.

```html
<title>Simply Tim | Where's Your Head At?</title>
```

The `<title>` provides:

1. The browser tab's text.
2. The default name if a user bookmarks the page.


---


## `<meta>`


This self-closing tag provides a single data point via the combination of two of its attributes. The `name` attribute is used to provide document-level metadata and **must** be complimented by the `content` attribute for its value. The `http-equiv` attribute simulates an HTTP response header.
`name="author"`, `name="application-name"` and `name="keywords"` don't seem to be useful anymore so I won't be using them in a rush. Let's go through some common use cases:


### `name="description"` 
```html
<meta name="description" content="Describe your document here">
```
Used in search engine results to give more information to potential visitors. *Ensure the most important information is in the first 160 characters of the description to avoid having the important suff chopped off when viewed in a search result.*


### `name="viewport"`
```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```
Crucial for responsive web design. I won't bloat this overview with all the details but needless to say if you're creating a responsive website, this meta tag is a must. With that in mind, if your site is not responsive then using this tag could worsen the user experience.


### `name="robots"`
```html
<meta name="robots" content="noindex, nofollow">
```
Provides guidance to [Web Crawlers](https://en.wikipedia.org/wiki/Web_crawler) as to how they should respond to this web page. In this example, crawlers are being asked to NOT index this page in their database and to NOT follow any links on this page. Again, there is a lot of depth to this tag which I'm not containing here.


### `http-equiv="content-type"`
```html
<meta http-equiv="content-type" content="text/html; charset=utf-8">
```
The character encoding declaration for the web page. There are different types of character encoding but UTF-8 covers almost all of the characters and symbols in the world and has become a no-brainer. In this case, the whole `<meta>` tag can be, and usually is, shortened down to:

```html
<meta charset="utf-8">
```


### `http-equiv="refresh"`
```html
<meta http-equiv="refresh" content="5 ; url=http://exampleSite.co.uk/">
```
As you may have guessed, this refreshes the web page after the specified amount of seconds (in this example it's 5 seconds). Optionally, and separated by a semicolon, this refresh can redirect the user to a given URL. *Note that when utilising the redirect functionality, both the time in seconds and the redirect URL are part of the same string as the value of `content`.*


---


## `<script>`


The `<script>` tag is used in two ways, both of which bring JavaScript into your web page.

1. Embedded JS: This method hard-codes JavaScript directly into your page. It is important to note that it can only affect the page within which it is embedded.
   ```html
   <script>
        //javascript code here
   </script>
   ```
2. External JS: This method is usually prefered over embedded. It allows you to store your JavaScript in a separate file which is then included in your page via the `src` attribute. This method empowers [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) coding because that .js file can be included like this across your whole website.
   ```html
    <script src="app.js"></script>
   ```

The location of the `<script>` tag in your HTML document is extremely important. This is because as a Web Browser parses your HTML, by default it halts when it comes to a `<script>` tag and executes the contained JavaScript before then parsing the rest of the HTML. If your JavaScript references the DOM, you want to ensure it is only executed once the DOM is fully accessible. There are two ways you can ensure this:

1. Place all your `<script>` tags right at the bottom of your page, just inside the `</body>` tag.
2. Include the boolean attribute `defer` which 'defers' (shock horror!) the execution of the script until the HTML page is fully parsed.
   ```html
    <script src="app.js" defer></script>
   ```

Another useful boolean attribute of the `<script>` tag is `async` which tells the browser to execute the Javascript asynchronously alongside the HTML.


---


## `<link>`

Another self-closing tag, `<link>` loads external resources such as CSS, favicons and fonts. Both the `href` and `rel` attributes *must* be used. `href` defines the address of the resource and `rel` defines its relationship: Single, Married or "It's Complicated". No not really. `rel` should be "stylesheet" or "icon" etc.

```html
<link href="app.css" rel="stylesheet">
<link rel="icon" href="myFavicon.ico">
```

The two examples here are about as basic as `<link>` tags can get. For more complicated `<link>` tags the `type` attribute would likely be required plus the optional use of many other attributes such as `sizes`.


---


## `<style>`

Similar to the `<script>` tag,  `<style>` should contain code, specifically CSS code, which is applied to that document only. Embedding CSS like this is not usually recommended. Referencing external stylesheets, conversely, cannot be done with the `<style>` tag but must be done using the `<link>` tag as mentioned above.

The `media` attribute can be used to apply the CSS conditionally using media queries such as those used in responsive design or print formatting.

```html
<style media="print">
    a {
        color: black;
    }
</style>
```


---


## `<base>`

This self-closing tag is not often required. It allows you to specify the base URL for the document. This means that **all** relative URLs contained within the document will be based off of this `<base>` tag. So unless you have a very deep and complicated webite structure, it probably isn't necessary.

```html
<base href="https://mysite.com">
```
If you do choose to use this tag it's probably best placing it first inside the `<head>` tag to ensure it affects all the document's relative URLs.


---


## Typical `<head>` Heirarchy
```html
<head>
	<base>
	<meta>
	<title>Simply Tim | Where's Your Head At?</title>
	<link>
	<style>
		/* Embedded CSS */
	</style>
</head>
```