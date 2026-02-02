# BioBlitz Project Instructions

## Phase 1: HTML

Please create a root folder for this project called "bioblitz" inside your OneDrive. Create the files and folders below.

### Site Layout

        Bioblitz Root folder
        |
        |- index.html
        |- img (folder)
            |- foreground/content/5Ws images (like jpegs from Unsplash)
        |- css 
            |- style.css
            |- reset.css
            |- bgimg (folder)  
                |- decorative background images called up by the css



- Following the example of the [CSS Zen Garden HTML](../01-review/csszengarden.com.html), take the [text-content.md](text-content.md) information and insert it into an HTML template based on this HTML structure:

        div.wrapper
            header <!-- visual branding -->
            main
                section.who <!-- target the audience -->
                    h2
                    div.flex-container
                        picture + img <!-- column 1 -->
                        div     <!-- column 2 -->
                    <!-- close flex-container div here -->
                
                section.what <!-- where does this happen -->
                    h2
                    div.flex-container
                        picture + img
                        div
                    <!-- close flex-container div here -->
                
                section.when <!-- when is the event -->
                    h2
                    div.flex-container
                        picture + img
                        div
                    <!-- close flex-container div here -->
                
                section.where <!-- where does this happen -->
                    h2
                    div.flex-container
                        picture + img
                        div
                    <!-- close flex-container div here -->
                
                section.how <!-- how does one participate? -->
                    h2
                    div.flex-container
                        picture + img
                        div
                    <!-- close flex-container div here -->
                
                section.why <!-- why does this event take place? -->
                    h2
                    div.flex-container
                        picture + img
                        div
                    <!-- close flex-container div here -->
            footer
        <!-- close wrapper div here -->

Each section will be divided into two elements (usually picture tags and divs) that will display as two columns on larger screens. [See this example of the completed HTML](./view-source-billypoppins-bioblitz.html) for reference.


### Note about inserting images

This semester we will be using the HTML 5 picture tag. It provides the means for the web browser to choose from a set of different img tags depending on certain conditions, such as if the mobile phone is held horizontally or vertically. The type of code is this:


#### Basic usage to start the exercise

        <picture>
            <img src="picturename.jpg" alt="a demo image">
        </picture>


 #### Responsive usage

        <picture>
            <source srcset="flowers-portrait.jpg" media="(orientation: portrait)">
            <source srcset="flowers-landscape.jpg" media="(orientation: landscape)">

            <img src="flowers.jpg" alt="Flowers">
            <!-- the img tag is used if the browser cannot display the sources written in the media queries -->
        </picture>


               

### Replace 5Ws 

Replace the words "why, what, where, when, why and how" with more appealing subtitles. [Compare this page](https://billypoppins.dev.graphicandwebdesign.ca/bioblitz/) with [this page](https://billypoppins.dev.graphicandwebdesign.ca/bioblitz/index-decorated.html).



### Add the images

For each section, [add a stock image](https://unsplash.com/) that represents the "why, what, where, when, why and how".

Using the collection of images you found to "answer the 5Ws":

- Place the images in the img folder (not the css/bgimg folder)
- Using an img tag, insert each image in the appropriate HTML section tag (ex: picture of Sainte-Anne-de-Bellevue in the "where" section)
- You will insert the images at full size now, but resize them later according to the sizes in use in your design.


Make sure to **validate your HTML** and fix any errors before going onto the next step.


## Phase 2: Mobile First CSS

### 2.1 CSS Reset

Use: [https://raw.githubusercontent.com/JACGWD/CSS-Reset-Selector/refs/heads/main/reset/simple-css-reset-v2.5.css](https://raw.githubusercontent.com/JACGWD/CSS-Reset-Selector/refs/heads/main/reset/simple-css-reset-v2.5.css)

Link to the reset file in the \<head> **above the link to the normal stylesheet. Resets must always come first!**

            <link rel="stylesheet" href="css/reset.css">
            <link rel="stylesheet" href="css/style.css">
        </head>


### 2.2 Choose your fonts

Take the time to research the type of fonts associated to the art style you have selected in the Design Theory class. This is particularly important for the font chosen for use in the headers. The body font should chosen for its complementary style, but also for its legibility at sizes between 12-16px.

Add three custom font choices:

1. H1 title (Main branding/identity)
2. Headers (h2 to h6)
3. Body text (all other texts)

#### Google Fonts How To

1. Go to [https://fonts.google.com/](https://fonts.google.com/)
2. Choose a font
3. Click "Get Font" at to right
4. Click "get Embed Code"
5. This part goes at the bottom of \<head> (the third line will be different depending on the fonts you choose):

        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Boldonse&display=swap" rel="stylesheet">

6. This code goes in your CSS:

        .boldonse-regular {  <-- change the class name to your choice of HTML tag(s) 
            font-family: "Boldonse", system-ui;
            font-weight: 400;
            font-style: normal;
        }

7. Your final fonts code should look something like this:

        body {   
            font-family: "Boldonse", system-ui;
            font-weight: 400;
            font-style: normal;
        }

        h1 {
            font-family: "Outfit", sans-serif;
            font-optical-sizing: auto;
            font-weight: 600;
            font-style: normal;
            } /* Use this font exclusively for the title/branding */

        h2,h3,h4,h5,h6,label,legend {   
            font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
            font-weight: bold;
            font-style: normal;
        }

### 2.3 Pick your font sizes for mobile

1. Make sure your choice of fonts are loading. Use Firefox's Font Inspector (in the web inspector toolbox) to see which fonts are active on the page.
2. Look at your page in **mobile view** size
3. Find the H1 and H2 tags
4. Use the web inspector to adjust the h1 size up or down until it fits nicely on the page, ex: 2.1rem
5. Go to the [Typographic Scale](https://spencermortensen.com/articles/typographic-scale/) and enter the value from the previous step (ex: 2.1) as the R value
6. Paste the CSS from the scale in your CSS



        h1 {
        font-size: 2.25em; /* adjust this value according to the size of your chosen font in your 320px mobile preview */
        }

        h2 {
        font-size: 1.9656em;
        }

        h3 {
        font-size: 1.7171em;
        }

        h4 {
        font-size: 1.5em;
        }

        h5 {
        font-size: 1.3104em;
        }

        h6 {
        font-size: 1.1447em;
        }

        p {
        font-size: 1em;
        }

        small {
        font-size: 0.8736em;
        }


### Section 2.4 Format the header

In this section, you format the size of the h1 text, the JAC logo and the negative space of the header.

#### Examples

Use the following examples as hints of which CSS rules to use. Do not copy them blindly as they probably don't apply to your layout.

        header {padding: 2rem;}

        #jac-logo {
            width: 100%;
            height: auto;
            display: block;
            filter: invert(1);  /* makes the black svg white if necessary */
            margin: 0rem auto;
        }

        h1 {
            font-family: "Outfit", sans-serif;
            font-optical-sizing: auto;
            font-weight: 900;
            font-style: normal;
            font-size: 5rem;
            text-align: center;
            margin: 1rem;
            }



### 2.5 Style Headings

Here we give the title and subtitles some basic formatting.

#### Examples

        h2,
        h3,
        h4,
        h5,
        h6 {
            font-weight: bold;
            line-height: 1.1;
            margin: 2rem 0 1rem 0;
        }




### 2.6 Choose your color palette

For this section, give a color to each text such as the H2 tags. Sections can have a background-color, border color and text color.


#### Examples

        section.classname h2 {
            color: black
            }

        section.classname {
            background-color: yellow;
            color: black;  /* color for non-link text, use LoVeHA rules below for link colors */
            border: 2px solid blue;
        }


#### CSS Selectors for assigning colors

        body {}

        div.wrapper {
            background-color: white;
        }

        header {}



        h1 {}

        h1 span {}

        header h2 {}



        section {} /* all sections together */

        section.who {}

        section.what {}

        section.what h2 {}

        section.when {}

        section.when h2 {}

        section.where {}

        section.where h2 {}

        section.how {}

        section.how h2 {}

        section.why {margin-bottom: 0;} /* last section */

        section.why h2 {}

        footer {}




### 2.7 LoveHA Rules

In this section, define the colors and visual attributes of text links. For example:

#### Example

        header a:link {color: white; text-decoration: none;}
        header a:visited  {color: rgb(220, 218, 218);}
        header a:hover  {text-decoration: underline;}
        header a:active {color: magenta;}



#### Required CSS selectors

        header a:link {}
        header a:visited  {}
        header a:hover  {}
        header a:active {}
        
        main a:link  {}
        main a:visited  {}
        main a:hover  {}
        main a:active  {}

        footer a:link  {}
        footer a:visited  {}
        footer a:hover  {}
        footer a:active  {}

Remember that the LoveHA rule not only defines colors but also defines basic interactivity. Effects like hover or states like visited give the user feedback about how they are using the page and where in the site they have been. Choose the colors and effects to best guide the user in visiting the site.


### 2.8 Heights, Widths, Margins & Padding

The most important part of the design-for-mobile process is **spacing elements apart**. 

- Add whitespace on the left and right edges so elements do not touch the edge of the screen.
  - padding: 1rem; on body {} or div.wrapper {}
  - or: margin: 1rem; on div.wrapper {} or section
- Add margin-top {} and margin-bottom {} to:
  - header (margin-top can be zero)
  - main
  - all sections
  - footer  (margin-bottom can be zero)

### 2.9 Format the picture element

Here we space the images away from the text that follows underneath.

        picture {
            margin: 0 0 1rem 0;
            display: block;
        }


### 2.10 Place smartphone logos side by side

        .how .flex-container {
            display: flex;  /* places the two anchor tags side by side */
            flex-basis: 50%;
        }

        .how .flex-container a {
            max-width: 50%; /* set the two anchors to act like two columns of 50% width */
            display: block;
            margin: 0 auto;
        }

        .android img {
            width: 200px;  /* adjust width of android logo */
            height: auto;
        }

        .ios img {
            height: 36px;  /* adjust height of ios logo */
            width: auto;
            position: relative;
            top: 8px;  /* align vertically */
        }


Congratulations, you have completed the mobile design!



## Phase 3: Multi-column Layout Using Media Queries for Larger Devices


### Going from Mobile Scale to Larger Viewports

#### Controlling Page Layout at Different Viewport Sizes: Media Queries

<blockquote>

1. Media: The technology used to transmit the content.
2. Query: A question.
3. "Media Query": The web browser asks the device's operating system what it is capable of, and displays the page accordingly.

</blockquote>

See: [https://www.w3schools.com/css/css3_mediaqueries_ex.asp](https://www.w3schools.com/css/css3_mediaqueries_ex.asp)

### Examples of How Media Queries Work

#### Rules for computer screens

    @media screen {
        h1 {color: red;}
    } 

#### Rules for formatting the page when printed    
    
    @media print {
        h1 {color: black;}
    }

#### Rules for computer screens that are taller than they are wide    
    
    @media screen and (orientation: portrait) {

        /* use tall background image */

    }

#### Rules for computer screens that are narrower than 640px
    
    @media screen and (max-width: 640px) {

        /* display navigation as hamburger menu */
    }


#### Rules for computer screens that are wider than 64rem
    
    @media screen and (min-width: 64rem) {

        /* display horizontal navigation menu */
    }

#### Rules for computer screens that are narrower than 640px and taller than they are wide
    
    @media screen and (max-width: 640px) and (orientation: landscape) {

        /* use small horizontal background image */
    }

### Mobile First

"Mobile first" is the simplest strategy for designing responsive web page.

1. Start with no media queries at all: Define all the styles for the mobile phone design.
2. Once the viewport is wide enough for **two columns** of content, use a media query that puts content side-by-side *starting at that width*.
3. Once the viewport is wide enough for **three columns** of content, use a media query that puts content side-by-side *starting at that width*.
4. Repeat as many times as necessary depending on how many columns you need.
5. Once you reach laptop/desktop widths, use a "wrapper" div (a fixed width box that surrounds all the content) to center the page contents.



### Setting elements side-by-side

#### Using Flex Box

##### The Basic Alignment

   @media screen and (min-width: 1024px) {
    .when .flex-container {
        display: flex;
        /* puts elements side-by-side */
    }
   } /* always comment closing media query */

or

    @media screen and (min-width: 1024px) {
        .when .flex-container {
            display: flow-root;
            /* wraps float */
        }
    
    .when .flex-container picture {
        float: left;
        /* puts elements side-by-side */
        }
    } /* always comment closing media query */


##### Switching the Items Order

    .when .flex-container {
        flex-direction: row-reverse;
        /* places elements in reverse order: last element becomes first */
    }

    or

    .when .flex-container picture {
        float: right;
        /* float to opposite side */
        }

##### Setting Column Width

    .when div,
    .when picture,
    .why div,
    .why picture {
	    flex-basis: 50%;
    }  /* for flexbox */

or
    .when div,
    .when picture,
    .why div,
    .why picture {
	    width: 50%;
    }  /* for floats */



#### Using CSS Grid

##### The Basic Alignment & Column Width

     .how .flex-container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        /* two columns: each equal to one fraction of the available space */
    }

##### Switching the Items Order

    .how picture {
        order: 2;
        /* force to go to column 2 */
      }

    .how .flex-container div {
        order: 1;
        /* force to go to column 1 */
    }


### Horizontal & Vertical Centering 

#### Using line-height (for a single line of text)

When you have a **single line of text**, you can vertically center it using a line-height equal to the height of the parent element. Then you can use regular text centering.

    footer {
        background-color: #2679d8;
        color: #fff;

        height: 5rem;
        line-height: 5rem;
        /* the **single line** of text is the same height as the box it is in: vertical centering */

        text-align: center;
        /* horizontal centering */
    }


#### Using Flex Box

    footer {
        background-color: #2679d8;
        color: #fff;
        height: 5rem;
        
        display: flex;

        align-items: center;
        /* vertical centering */

        justify-content: center;
        /* horizontal centering */
    }


#### Flex

Use a media query to make items go side by side using display: flex and display: grid.

See: [https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#setting-elements-side-by-side](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#setting-elements-side-by-side)

### Alternate the position of some items

See: [Flexbox](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#switching-the-items-order) and [CSS Grid](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#switching-the-items-order-1)

## Step 9: Add CSS background images

See: [Point 6 on this page](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8-notes.md)


## Testing Setup

Use this page to load your page multiple times into iframes of different sizes so you can observe the media queries in action. Requires PHP: use the [wordpressplayground.wordpress-playground VS Code extension](https://marketplace.visualstudio.com/items?itemName=WordPressPlayground.wordpress-playground)

[https://github.com/JACGWD/Responsive-iFrames](https://github.com/JACGWD/Responsive-iFrames)




#### Three fonts: Brand, headers, body
- Find longest title, choose h1 size accordingly for mobile
- Use type scale to find intermediates

### Color palette

Define color variables:

#### header

- Header background color
- Header text color
- Header anchor LoVeHA

#### main

- Main background color
- Main text color
- Main anchor LoVeHA

#### footer

- Footer background color
- Footer text color
- Footer anchor LoVeHA



### Notes on Typography

#### The Ideal Line Length
- [https://baymard.com/blog/line-length-readability](https://baymard.com/blog/line-length-readability)

#### Line Length in Web vs Print
- [https://www.viget.com/articles/the-line-length-misconception/](https://www.viget.com/articles/the-line-length-misconception/)

#### Examples of CSS for Limiting Line Length

    p { 
        max-width: 85ch; 
        /* paragraph only */
    } 

    or

    h1,
    h2,
    h3,
    h4,
    h5,
    h6,
    legend,
    label,
    p,
    li { 
        max-width: 100ch; 
        /* most on-screen text */
    }  


## Technical Review

- Q: What is the image size?
- Q: What is the text measure width? 