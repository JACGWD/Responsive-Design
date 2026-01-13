# BioBlitz Project Review

## Step 1: Copy my content

1. If do not have a complete page of HTML yet, copy the code from the demo. See: [text-content.md](text-content.md) and [view HTML source demo](./view-source-billypoppins-bioblitz.html)
2. You can adjust the text and code as you feel appropriate.


## Step 2: CSS Reset

Add the CSS Reset in order to remove the white border around the frame. You can paste the reset code at the top of the CSS stylesheet. Or link to it in the \<head> **above the link to the normal stylesheet. **Resets must always come first!**

See: [https://raw.githubusercontent.com/JACGWD/CSS-Reset-Selector/refs/heads/main/reset/simple-css-reset-v2.4.css](https://raw.githubusercontent.com/JACGWD/CSS-Reset-Selector/refs/heads/main/reset/simple-css-reset-v2.4.css)

### Most important rule for responsiveness

This rule forces your images to scale down to fit the artboard/viewport.

        img {
            max-width: 100%;
            height: auto;
        }

## Step 3: Replace 5Ws 

Replace the words "why, what, where, when, why and how" with more appealing subtitles. [Compare this page](https://billypoppins.dev.graphicandwebdesign.ca/bioblitz/) with [this page](https://billypoppins.dev.graphicandwebdesign.ca/bioblitz/index-decorated.html).

## Step 4: Add Content Images

For each section, [add a stock image](https://unsplash.com/) that represents the "why, what, where, when, why and how".

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

Add two custom font choices:

1. Headers
2. Body text

### Google Fonts How To

1. Go to [https://fonts.google.com/](https://fonts.google.com/)
2. Choose a font
3. Click "Get Font" at to right
4. Click "get Embed Code"
5. This part goes at the bottom of \<head>:

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
2. Look at your page in mobile view
3. Find the H1 and H2 tags
4. Use the web inspector to adjust the h1 size up or down until it fits nicely on the page, ex: 2.1rem
5. Go to the [Typographic Scale](https://spencermortensen.com/articles/typographic-scale/) and enter 2.1 as the R value
6. Paste the CSS from the scale in your CSS
7. You can readjust the font sizes for bigger screens using [media queries](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#examples-of-how-to-use-media-queries).

## Step 7: Flex

Use a media query to make items go side by side using display: flex and display: grid.

See: [https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#setting-elements-side-by-side](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#setting-elements-side-by-side)

## Step 8: Alternate the position of some items

See: [Flexbox](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#switching-the-items-order) and [CSS Grid](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#switching-the-items-order-1)

## Step 9: Add CSS background images

See: [Point 6 on this page](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8-notes.md)