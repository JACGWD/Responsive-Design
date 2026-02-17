# Class Notes 5.1

![CSS Box Model](../01-review/img/css-box-model.png)

## How to Center a *Block Level* Element

    div {
        width: 250px; /* a width must be set */
        margin: 0 auto;  /* top/bottom value is unimportant; the left/right margins must be set to automatic */
    }    


## How to Center a *Inline* Element

    img {
        width: 250px;
        margin: 0 auto;
        display: block;  /* element must be set to block (or inline-block) so the width can be set */
    }        


## Padding

We need to make sure that our text content does not touch the edge of the screen. 

        header {
            padding: 1rem;
        }


        /* use either main or section below, not both  */
        
        main  {
            padding: 1rem; /* this will push every section (and its background color) inwards */
        }

        section {
            padding: 1rem; /* lets the background color touch the edge of the screen */
        }

        footer {
            padding: 1rem;
        }


## Place smartphone icons side-by-side

[https://github.com/JACGWD/Responsive-Design/blob/main/bioblitz/instructions-2-mobile.md#210-place-smartphone-logos-side-by-side](https://github.com/JACGWD/Responsive-Design/blob/main/bioblitz/instructions-2-mobile.md#210-place-smartphone-logos-side-by-side)