# BioBlitz Project Instructions

## Phase 1: HTML

- Following the example of the [CSS Zen Garden HTML](../01-review/csszengarden.com.html), take the [text-content.md](text-content.md) information and insert it into an HTML template based on this HTML structure:

        div.wrapper
            header <!-- visual branding -->
            main
                section.who <!-- target the audience -->
                    picture <!-- column 1 -->
                    div     <!-- column 2 -->
                section.what <!-- where does this happen -->
                    picture
                    div
                section.when <!-- when is the event -->
                    picture
                    div
                section.where <!-- where does this happen -->
                    picture
                    div
                section.how <!-- how does one participate? -->
                    picture
                    div
                section.why <!-- why does this event take place? -->
                    picture
                    div
            footer
        <!-- close wrapper div here -->

Each section will be divided into two elements (usually pictures and divs) that will display as two columns on larger screens. [See this example of the completed HTML](./view-source-billypoppins-bioblitz.html) for reference.

### Replace 5Ws 

Replace the words "why, what, where, when, why and how" with more appealing subtitles. [Compare this page](https://billypoppins.dev.graphicandwebdesign.ca/bioblitz/) with [this page](https://billypoppins.dev.graphicandwebdesign.ca/bioblitz/index-decorated.html).

Make sure to **validate your HTML** and fix any errors before going onto the next step.


### Add the images

For each section, [add a stock image](https://unsplash.com/) that represents the "why, what, where, when, why and how".

Using the collection of images you found to "answer the 5Ws":

- Place the images in the img folder (not the css/bgimg folder)
- Using an img tag, insert each image in the appropriate HTML section tag (ex: picture of Sainte-Anne-de-Bellevue in the "where" section)
- You will insert the images at full size now, but resize them later according to the sizes in use in your design.


## Phase 2: Mobile First CSS

### CSS Reset

Use: [https://raw.githubusercontent.com/JACGWD/CSS-Reset-Selector/refs/heads/main/reset/simple-css-reset-v2.4.css](https://raw.githubusercontent.com/JACGWD/CSS-Reset-Selector/refs/heads/main/reset/simple-css-reset-v2.4.css)

Link to the reset file in the \<head> **above the link to the normal stylesheet. Resets must always come first!**

            <link rel="stylesheet" href="css/reset.css">
            <link rel="stylesheet" href="css/style.css">
        </head>


### Choose your fonts

Add two custom font choices:

1. Headers (h1 to h6)
2. Body text (all other texts)

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

        h1,h2,h3 {   
            font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
            font-weight: bold;
            font-style: normal;
        }

#### Pick your font size for mobile

1. Make sure your choice of fonts are loading 
2. Look at your page in mobile view size
3. Find the H1 and H2 tags
4. Use the web inspector to adjust the h1 size up or down until it fits nicely on the page, ex: 2.1rem
5. Go to the [Typographic Scale](https://spencermortensen.com/articles/typographic-scale/) and enter 2.1 as the R value
6. Paste the CSS from the scale in your CSS
7. You can readjust the font sizes for bigger screens using [media queries](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#examples-of-how-to-use-media-queries).


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


### Choose your color palette

For this section, give a color to each text such as the H2 tags. Sections can have a background-color, border color and text color.


#### Example

        section.classname h2 {
            color: black
            }

        section.classname {
            background-color: yellow;
            color: black;  /* color for non-link text, use LoVeHA rules for link colors */
            border: 2px solid blue;
        }


#### CSS Selectors for assigning colors

        body {}

        div.wrapper {
            background-color: white;
        }

        header {}

        header a:link {}
        header a:visited  {}
        header a:hover  {}
        header a:active {}

        h1 {}

        header h2 {}

        main a:link  {}
        main a:visited  {}
        main a:hover  {}
        main a:active  {}

        section.who {}

        section.what {}

        section.what h2 {}

        section.when {}

        section.when h2 {}

        section.where {}

        section.where h2 {}

        section.how {}

        section.how h2 {}

        section.why {}

        section.why h2 {}

        footer {}

        footer a:link  {}
        footer a:visited  {}
        footer a:hover  {}
        footer a:active  {}


### Heights, Widths, Margins & Padding

The most important part of the design-for-mobile process is spacing elements apart. 

- Add whitespace on the left and right edges so elements do not touch the edge of the screen.
  - padding: 1rem; on body {} or div.wrapper {}
  - or: margin: 1rem; on div.wrapper {} or section
- Add margin-top {} and margin-bottom {} to:
  - header (margin-top can be zero)
  - main
  - all sections
  - footer  (margin-bottom can be zero)



## Phase 3: Multi-column Layout Using Media Queries for Larger Devices




## Step 5: Add CSS colors

Following the decisions you took in Figma, add your choice of background colors to:

    body {
        background-color: #444;
    }

    header {
        background-color: #FFF;
    }

    footer {
        background-color: #444;
    }

## Step 6: Add custom fonts



## Step 7: Flex

Use a media query to make items go side by side using display: flex and display: grid.

See: [https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#setting-elements-side-by-side](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#setting-elements-side-by-side)

## Step 8: Alternate the position of some items

See: [Flexbox](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#switching-the-items-order) and [CSS Grid](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#switching-the-items-order-1)

## Step 9: Add CSS background images

See: [Point 6 on this page](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8-notes.md)


## Testing Setup

Use this page to load your page multiple times into iframes of different sizes so you can observe the media queries in action. Requires PHP: use the [wordpressplayground.wordpress-playground VS Code extension](https://marketplace.visualstudio.com/items?itemName=WordPressPlayground.wordpress-playground)

[https://github.com/JACGWD/Responsive-iFrames](https://github.com/JACGWD/Responsive-iFrames)




## Assignment: Mobile

1. Create a standard html page
2. Add style tag inside head
3. Add multiple images using orientation media query and 1x + 2x resolutions. Image width is defined by column width in Figma. 
4. Remember that 2x images must be saved from same size or bigger images. **Not scaled up from smaller sizes.** 
5. Wrap elements (picture + picture, picture + text, etc) that will be side by side on larger screens inside a div. Use a "flex-container" class. 

### Fonts

- Find Legal typefaces
- Adobe
- Google

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