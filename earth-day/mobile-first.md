# Mobile First

## The proper way to start a web project

1. Choose a visual theme based on climate
2. Choose your fonts at [Google fonts](https://fonts.google.com/) or [Adobe](https://fonts.adobe.com/)
3. Add a [typographic scale](https://spencermortensen.com/articles/typographic-scale/)
4. Define a color palette using [CSS variables](https://www.w3schools.com/css/css3_variables.asp)
5. Extract colors from images at [https://color.adobe.com/create/image](https://color.adobe.com/create/image) 
6. Start building a library of background images based on your theme. Save them into the css/bgimg folder.

### Intro to CSS Grid

We want to minimize the visual importance of the 17 UN icons so we will display them in four columns.

        .earthday .flex-container {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr 1fr;
            gap: 0.25rem;
            margin: 0.25rem;
        }


### Edit JAC logo

We want to be able to control both instances of the JAC logo with one CSS rule. If we have two IDs with the same name we will get a validation error. So we will use a class. We will change the JAC ID to a class from this:

        <img src="img/Logo_JAC-Horiz_K.svg" alt="John Abbott College logo" id="jac-logo">

to this:

        <img src="img/Logo_JAC-Horiz_K.svg" alt="John Abbott College logo" class="jac-logo">

Then find the JAC logo in the .logos section and add the missing class there too.

        <li><img src="img/Logo_JAC-Horiz_K.svg" alt="John Abbott College Logo"></li>

to

        <li><img src="img/Logo_JAC-Horiz_K.svg" alt="John Abbott College Logo"  class="jac-logo"></li>



 ### Assign background color values to each section by class

 You can also add a "color" value to the text tag, such as paragraph.


        .giveaway {
            background-color: var(--blue1);
        }

        .giveaway p {
            color: var(--mauve);
        }

        .macmarket {
        background-color: var(--blue2);
        }

        .gwd {
        background-color: var(--blue3);
        }

        .transplant {
        background-color: var(--blue1);
        }

        .logos {
        background-color: var(--mauve);
        }

        .earthday {
        background-color: var(--blue2);
        }     

        .macmarket h2,
        .macmarket h3,
        .earthday h2,
        .earthday h3 {
        color: var(--white);   
        }


### Add default spacing for the sections and header        


        section {
            margin: 2rem auto;
            padding: 1rem;
        }

        header{
            padding: 1rem;
        }




### Invert the logos if necessary

If you assign a dark background color to the .logos container, you will want to make the black logos white. But you will not want to invert the McGill logo which is the fourth item in the list of logos.


        .logos .two img {
            filter: invert(100%);
        }

        .logos .two li:nth-child(4) img {
            filter: none !important;
        }

### Set width of logos


        .logos .two li {
            margin: 1rem auto; /* margin for all logos */
        }

        .logos .two li:nth-child(1) {
            width: 80%;  /* width for first logo */
        }

 ## Continue to the first media query

 Continue the project by [implementing the first media query.](./first-media-query.md)       