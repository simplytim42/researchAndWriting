# Structurally-Semantic HTML

When it comes to semantic HTML there is a lot to choose from. This article focuses on the high-level, structurally-semantic elements `<main>`, `<header>`, `<footer>`, `<section>`, `<article>`, `<nav>` and `<aside>`.

## Bit 'o' Context

The Section Elements were a *two-birds-one-stone* kinda deal!

* Bird 1: Prior to their implementation, developers would wrap related content in a div and give it a class of 'header', or 'footer' or 'nav' etc. So making them official was very much a commonsensical paving of the cow paths.
* Bird 2: Making it an official implementation in the HTML5 specification bolstered the ability to give semantic meaning to these elements across all client devices which provided a much needed contribution to web accessability.

## `<main>`
With such a vast range of 'stuff' on the average web page, the `<main>` element lets you get straight to the point! It acts like a big flag embroidered with the words 'THIS STUFF HERE IS THE REAL REASON YOU CLICKED ON THIS PAGE'.  

There should only be one `<main>` per page and its content should be unique to the page (otherwise it wouldn't be the *main* bit now would it). Ideally, it should not be nested inside any other element other than `<body>`.

## `<header>`
This element should contain *introductory material*. Unlike the `<main>` element, there is no reason to limit yourself to just the one. But don't go getting all greedy, use them sensibly: it usually makes sense to have a `<header>` near the top of the page or at the start of a `<section>` or `<article>`.

The rules on what should go inside a `<header>` are very much subjective to the content. If some content makes sense as a block of introductory goodness, then pop it inside a `<header>`. You'll find that a generic use of this element is to have it contain a company logo, site title and the top-level navigation. On a blog or newspaper site you'll likely find an `<article>` element contains a `<header>` which houses the article's title, date and author.

## `<footer>`
The great equaliser of the `<header>`, this element is for the content you typically find at the bottom of a page or article or section. We're talking copyright information, related documents, not-so-primary navigation, author details etc. Maybe an article is part of a series, in which case you may choose to give the article a `<footer>` containing navigation to the next and previous articles.

## `<aside>`
The best definition I've come across for the `<aside>` is 'content that is separate from, but tangentially related to, the surrounding content'. Things like background information, pull quotes (like the one below) etc. Something that may be of interest to the user but not critical to the rest of the content. Think of it this way: if all the `<aside>` elements across the whole of the internet suddenly evaporated into the 'outernet' (see what I did there), then no web page should be any less useful. Every web page should still be legible and relevant.

> If all the `<aside>` elements across the whole of the internet suddenly evaporated into the 'outernet' (see what I did there), then no web page should be any less useful."

## `<nav>`
It is customary to use an unordered list to structure your site navigation. Wrapping this list in the `<nav>` element ensures there is no misunderstanding of its purpose, especially for accessibility technology. 

But before you get all `<nav>` trigger-happy, understand that it should be used for primary site navigation and navigation for long articles or documents. The kind of navigation you typically store in a `<footer>` would not need to sit inside a `<nav> ` block.

## `<article>`
Defined as a 'self-contained work that could stand alone'. Imagine if everything else on your page disappeared and the only thing left is an `<article>`. This content, all on its lonesome, should still make sense. Commonly used to encompass a blog post, or individual blog comments, or a newspaper article.  

Your situation may not be as generic as that. [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article) gives an example of a weekly weather forecast being an `<article>` with each individual daily forecast inside it *also* being its own `<article>`. If we pick any one of these `<article>` elements and remove all other content it would be legible. Use this Isolation Test as a way to ensure you make the right decision about using the `<article>` element in your own project.

## `<section>`
A lot of content can easily be chunked into 'sections'. From chapters in a book to different types of news on a news website. This is where `<section>` comes into play. It can be summarised as containing a *'thematic group of content'*. As the name suggests, one `<section>` should make up one part of a group of sections related to each other in some way. Let's look at some examples.

1. You have written an article detailing in great depth your Top Ten Doctor Who episodes (obviously), each episode you write about would be a `<section>` in your article, the article itself is the whole, which has been chopped up into thematically related chunks called episodes. Each episode deserves a little independence, but doesn't really have a purpose without the article itself as context.
2. In the news website example, the site may have three columns containing the latest headlines of articles. The first columns could be *'Local News'*, the second *'World News'* and the third *'Bizarre News'*! Each `<section>` in this case represents the headlines in a specific area of news.

## A Note on Your Specific Situation
It's all fine and dandy to lay out these elements and the rules that govern them. But it's worth recognising that because the web is home to such a vast spectrum of sites and apps all trying, and hopefully succeeding, to solve every problem conceivable, having *'one specification to rule them all'* will sometimes leave grey areas: your specific situation may not have a black and white solution. You may need to hash out a few ideas with a work friend or mentor and come up with a *best fit* for your needs. 

As an example, whilst nosily looking at the html of some MDN articles, I noticed that they utilise the `<article>` element to wrap around the content of the page but the title of the article itself is often contained inside a `<header>` above the `<article>` and just inside the `<main>`.