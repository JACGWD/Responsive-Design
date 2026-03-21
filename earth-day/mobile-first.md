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