# How to use CSS Floats for Basic Page Layout

Floating elements is mostly a deprecated way of doing CSS page layout. The only floating technique still in common use is for wrapping text around images. Floats are presented here for pedagogical purposes regarding the relationship of elements within—or outside of—the normal text flow.


## Step by Step

1. Open the "floats-page-layout-exercise" folder that you downloaded from Omnivox in VS Code.
2. Open the index.html file in VS Code
3. Open the css/style.css file in VS Code
4. In the Explorer panel, right-click the index.html file and select "Open with Five Server".


### 2. Mobile First CSS

In modern web design, we **always design for the smartphone first**. In this case, we want the images to be centered.

        img {
            margin: 1rem auto;
            }


### 3. Add a Media Query

When the screen width is wide enough to hold two images side-by-side, we start the tiling of the images into multiple columns. 

#### 3.1 In CSS, when we want to apply style rules only when certain conditions (like the width of the screen) are met, we use a **media query**.


Add this CSS to the **very bottom** of the style.css file:


        @media screen and (min-width: 582px) {

            /* css rules go here */

        }  /* always comment the closing bracket of the media query so you don't confuse the closing bracket of the last CSS rule with the closing bracket of the media query */



<blockquote>

### IMPORTANT

All the CSS in the steps below are the be written **inside the media query's brackets**. 

These rules are *conditional*. We want them to apply only if there is enough room for two columns.


</blockquote>


### 4. Place the Slogan & Logo Side-by-Side

4.1 In the style.css file, write the following:

        .slogan {
            float: left; 
            margin-right: 1rem;
            }


Notice how the logo image rises up in the empty space next to the slogan. The header still wraps around the image because it is still in the text flow.


### 5. Place the Navigation Links Side-by-Side


5.1 In the style.css file, write the following:

        .navigation li {
            float: left; 
            margin-right: 1rem;
            }


Notice how the links merge into the pink background color of the \<article> tag that is coded below the \<nav> tag. This is because the \<nav> tag is collapsing due to the fact that all its child elements are floated, ie are taken out of the text flow.

To fix this we must use the **clearfix hack** which will force the parent element to wrap around the floating child elements.

5.2 In the index.html file, find the following line of HTML:

        <ul class="navigation">

and add the clearfix class name to it:

        <ul class="navigation clearfix">



### 6. Display the Images in Multiple Columns

In this section, we want to float the images to the left so that they remain in the normal left-to-right reading order.


6.1 In the style.css file, write the following:

        section img {
            float: left; 
            margin: 1rem;
            }

Notice how the \<section> tag (with the blue border) collapses and does not contain the floats. And the pink sidebar rises up underneath the images. This is because the section is not wrapping the floats.


6.2 In the index.html file, find the following line of HTML:

        <section>

and add the clearfix class name to it:

        <section class="clearfix">


Note that the images now tile into multiple columns within the section tag that has a white background/blue border.

**Also note that the number of columns depends on the width of the screen.**


### 7. Wrap the Text Around the Image in the Sidebar


7.1 In the style.css file, write the following:

        aside img {
            float: right; 
            margin: 0 0 1rem 1rem;  /* top right bottom left */
            }

Note that the image is taller than the \<aside> box because the box only wraps the text, not the image. 


7.2 In the index.html file, find the following line of HTML:

        <aside>

and add the clearfix class name to it:

        <aside class="clearfix">


Note that the yellow box with the red border now wraps around the image in the sidebar. 



### 8. Limit the Width of the Container

<blockquote>

### IMPORTANT

Limiting the overall width of the element that holds the basic content boxes (ex: \<main> is the parent of \<article> and \<aside>) is the key to making your page layout look professional.

Otherwise, your page becomes too wide on desktop screens and the mobile-optimized layout loses it's visual consistency.

In other words, your portrait-oriented rectangular mobile design should never be allowed to become an excessively wide (and very short) landscape-oriented rectangle. As a designer you want to impose a limit as to how wide is acceptable.

</blockquote>


8.1 For this we will add another media query:

        @media screen and (min-width: 886px) {
        
        main {
            max-width: 886px; /* wide enough for three columns */
            padding: 1rem;
            margin: 0 auto;
        }

        }  /* always comment the closing bracket */
