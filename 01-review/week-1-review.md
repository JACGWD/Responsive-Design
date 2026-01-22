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

### \<img>

Reference to an external image file that is embedded in the page. Note that an image is an **inline element**. 


### Basic Text Tags

#### \<h1>

The title of the page, within the body tag. There should only be one H1 on a page (because a web page should be only about one thing).

#### \<h2> to \<h6>

Various levels that breakdown structured information into an **organized hierarchy** of categories. For example:

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

#### \<p>

Paragraph: a block of text that explains one idea. 

#### \<ol>

An **ordered list**. Each list item is preceded by a number. The elements in the list are meant to be followed in a specific order: first to last.

#### \<ul>

An **unordered list**. Each list item is preceded by a bullet, circle or other decorative symbol. The elements in the list can be followed in any order.

#### \<li>

One line in any type of list.

### Structural Tags

#### \<header>

- The main "branding" part of the web page, at the very top. Usually contains the logo, and site name. Sometimes includes navigation, search and other useful elements.
- The decorative top part of an \<article> or blog post, often one of several, on a web page. Helps the reader choose which post to read amongst the several available on that page.

#### \<nav>

Tag that wraps all the different bits of code used as a navigation bar. For example, the nav tag will wrap a button and a list together to identify their purpose on the page.

#### \<main>

The box that holds the most important part of the page. For example if the web page is about dogs, all the text and pictures about dogs will go inside the main tag.


#### \<aside>

The box that holds information that is only somewhat related to the main purpose of the page. For example if the web page is about dogs, the aside will offer links to pages about other types of pets, such as cats and ferrets.

#### \<footer>

The bottom-most part of a web page. Usually contains links to the least interesting parts of the web site such as privacy policy, copyright notice, the site map, etc. In other words, the boring stuff. However, the footer is often a place where designers have a lot of graphic design fun, just to make it less boring.


#### \<section>

A part of the page that is different in content than other parts of the page. For example, on an Animals page you can have sections for cats and dogs. A section must have a subtitle within it in order ot be considered valid HTML.


### Generic Structural Tag

### \<div>

A "division" that means "this part of the html is different from the other parts". A generic box that serves no particular purpose. Often used to regroup elements that will be displayed side-by-side on one line when the page is viewed on larger screens.


## HTML & CSS Validation

- The process of running your HTML or CSS code through a software that checks for errors.
- Particularly important for CSS, as even the smallest CSS error can cause big display problems on the page.

## CSS Reset

A CSS stylesheet that removes any default styles built into the web browser, and also applies some modern defaults. The purpose of using a CSS Reset is to eliminate tiny variations&emdash;such as differences in margins&emdash;in between different browsers. This makes the rendering of the design more consistent in between browsers (and devices) and reduces the risk of the design appearing broken on certain systems.

**Things you may find in a CSS reset:**

        *,
        *::before,
        *::after {
        box-sizing: border-box;  /* the border-box fix applied to everything */
        }

        * {
         margin: 0; 
         padding: 0;  /* margins and padding of all elements set to zero */
         }

        img {
            max-width: 100%;  /* responsive images that scale down to fit smaller screens */
            height: auto;
        } 

## CSS Selectors

See: [https://www.w3schools.com/cssref/css_selectors.php](https://www.w3schools.com/cssref/css_selectors.php)

| CSS Selector  |  Selector Type | Description  |
|------------------ | --------------------- | --------------------- |
| p                               | Simple selector | Selects all HTML paragraph tags    |
| div p                           | Descendant combinator | Selects any paragraph inside a div (child, grandchild or more) |
| div > p                         | Child combinator | Selects every \<p> element that are direct children of a \<div> element, not grandchildren or more | 
| .caption                        | Class selector | Selects all elements named with class="caption" |
| #student                        | ID selector | Selects all elements with an id="student" |
| class                           | common | Used to mark an element so it can be differentiated from other elements of the same type. Ex: \<p class="caption"> vs \<p class="introduction">. The same class can be used multiple times on a page. |
| identifier                      | unique | Used to target one specific and unique element on a page, just like using an ID number to identify one specific student. A particular ID (ex: #1234) can exist only once on a page. But you can use multiple IDs on a page (ex: #1234 and #4567). Using classes or IDs to target elements makes no difference in CSS. Javascript however relies on the uniqueness of IDs for most effects. |



## Concepts Seen in the Review Videos

### CSS Box Model

![CSS Box Model](./img/css-box-model.png)

| Concept | Example / Comment |
| -------- | ------ |
| Normal flow, aka "Text flow" | Elements appear on screen in the order they are written in the HTML code |
| Block level element | p, div, section, header, footer, aside, main, ul, li, etc |
| Inline element | a, span, img |
| display: block | Force an inline element to display as a block |
| display: inline | Force a block level element to display inline  |
| display: inline-block | Force any element to display as an inline-block |
| display: flex;  | new material for second semester |
| display: grid;  | new material for second semester |
| box-sizing: content-box; | old default, troublesome |
| box-sizing: border-box;  | modern standard, part of CSS Resets |
| padding | white space between content and border. **Cannot be a negative value.** |
| margin | whitespace outside the border, between different elements. *Can be a negative value.*  |
| margin collapse | overlapping margins combine into one, using the width of the widest of the two margins |
| Fixed element width + margin: (some value) **auto;** |  Setting an element to a fixed width and with automatic left/right margins will horizontally center the element |
| position: relative;  | Positions an element relative to it's original position in the normal flow (before top/right/bottom/left values are applied). Use this to anchor a parent element so its absolutely positioned child element is positioned from the edges of the parent. Good for small alignment tweaks. Large amounts of offset will result in overlapping elements. |
| position: absolute; | Breaks the normal text flow by placing an element on a layer. Elements written below that element in the HTML **rise up** to fill the  space left empty when the element is moved onto a layer.  |
| z-index; | Define on which number layer to place an absolutely positioned element. Can be negative (towards the background) or positive (towards the reader). |
| absolute or fixed positioned elements | By default, these elements will be the **width of the content only** unless you explicitly define a width in your CSS. |