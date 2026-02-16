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

Replace the words "who, what, where, when, why and how" with more appealing subtitles. [Compare this page](https://billypoppins.dev.graphicandwebdesign.ca/bioblitz/) with [this page](https://billypoppins.dev.graphicandwebdesign.ca/bioblitz/index-decorated.html).



### Add the images

For each section, [add a stock image](https://unsplash.com/) that represents the "why, what, where, when, why and how".

Using the collection of images you found to "answer the 5Ws":

- Place the images in the img folder (not the css/bgimg folder)
- Using an img tag, insert each image in the appropriate HTML section tag (ex: picture of Sainte-Anne-de-Bellevue in the "where" section)
- You will insert the images at full size now, but resize them later according to the sizes in use in your design.


Make sure to **validate your HTML** and fix any errors before going onto the next step.

[Continue to the mobile design phase](./instructions-2-mobile.md)