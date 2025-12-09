# Review

## Root folder

The folder that contains the web site (where the home page file is located).

On the CPanel server the root folder is **public_html**

## Basic HTML Tags

Hyper Text Markup Language is a set of tags added to text to define the structure of a page of text. (Computers don't understand the meaning of the text. The tags add context to the blocks of text. The text itself is just scanned for keywords.)

### \<html>

Define the start and end of the entire web page.

### \<head>

The information about the page (title, description, author, etc) and instructions for the browser (links to other important files like stylesheets and fonts, etc).

### \<title>

The title of the document **for software**: It will be used as the page name title of browser window or tab, title of a bookmark, name in your favourites, as the result on a Google search page, etc. 

### \<body>

The content part of the web page, meant to be read by humans. (Bots will also read the page to scan for keywords, then link to it when a search matches the keywords.)

### \<h1>

The title of the page, within the body tag. There should only be one H1 on a page (because a web page should be only about one thing).

### \<h2> to \<h6>

Various levels that breakdown structured information into **organized** categories. For example:

    Animals (h1)
    |-- Mammals (h2)
        |-- Dogs (h3)
            |-- Terriers (h4) 
                |-- French Terriers (h5)
                |-- Bull Terriers (h5)
                    |-- Adults (h6)
                    |-- Puppies (h6)
    |-- Birds (h2)
          |-- Eagles (h3)
                |-- Bald Eagles (h4)
                |-- Royal Eagles (h4)

### \<p>

Paragraph: a block of text that explains one idea. 

### \<ol>

An **ordered list**. Each list item is preceded by a number. The elements in the list are meant to be followed in a specific order: first to last.

### \<ul>

An **unordered list**. Each list item is preceded by a bullet, circle or other decorative symbol. The elements in the list can be followed in any order.

### \<li>

One line in any type of list.

### \<img>

Reference to an external image file that is embedded in the page.

### \<header>

- The main "branding" part of the web page, at the very top. Usually contains the logo, and site name. Sometimes includes navigation, search and other useful elements.
- The decorative top part of an \<article> or blog post, often one of several, on a web page. Helps the reader choose which post to read amongst the several available on that page.

### \<nav>

Tag that wraps all the different bits of code used as a navigation bar. For example, the nav tag will wrap a button and a list together to identify their purpose on the page.

### \<main>

The box that holds the most important part of the page. For example if the web page is about dogs, all the text and pictures about dogs will go inside the main tag.


### \<aside>

The box that holds information that is only somewhat related to the main purpose of the page. For example if the web page is about dogs, the aside will offer links to pages about other types of pets, such as cats and ferrets.

### \<footer>

The bottom-most part of a web page. Usually contains links to the least interesting parts of the web site such as privacy policy, copyright notice, the site map, etc. In other words, the boring stuff. However, the footer is often a place where designers have a lot of graphic design fun, just to make it less boring.

### \<div>

A "division" that means "this part of the html is different from the other parts". A generic box that serves no particular purpose. Often used to regroup elements that will be displayed side-by-side on one line when the page is viewed on larger screens.

### \<section>

A part of the page that is different in content than other parts of the page. For example, on an Animals page you can have sections for cats and dogs. A section must have a subtitle within it in order ot be considered valid HTML.

## Validation

- The process of running your HTML or CSS code through a software that checks for errors.
- Particularly important for CSS, as even the smallest CSS error can cause big display problems on the page.

## CSS Selectors

Play this game to review and learn: [https://flukeout.github.io/](https://flukeout.github.io/)