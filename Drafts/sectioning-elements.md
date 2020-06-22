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

The rules on what should go inside a `<header>` are very much subjective to the content. If some content makes sense as a block of introductory goodness, then pop it inside a `<header>`. You may find a generic use of this element is to have it contain a company logo, site title and the top-level navigation. On a blog or newspaper site you'll likely find the `<article>` elements contains a `<header>` which houses the article's title, date and author.

## `<footer>`
The great equaliser of the `<header>`, this element is for the content you typically find at the bottom of a page or article or section. We're talking copyright information, related documents, not-so-primary navigation, author details etc. Or maybe an article is part of a series, in which case you may choose to give the article a `<footer>` containing navigation to the next and previous articles.

## `<section>`










## A Note on Examples
Instead of fluffing out this article with a finite amount of examples detailing exactly what kind of content should go inside each element, I believe you will get much more out of digging through the web and viewing the HTML of existing sites to see what they have done. The web contains such a spectrum of content that many different sites and apps will implement them in their own, hopefully correct, way. 