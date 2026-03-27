# First media query

Add the first media query. We will use a breakpoint of 60rem (960px):


        @media screen and (min-width: 60rem) {

        } /* close media query */


## A different kind of containing box

In this exercise, we will not use the wrapper div to constrain the content to a certain width. We want the sections to reach the edge of the screen so that the background color can reach the edge.

We will leave the sections at 100% width (possibly with a tiny margin). But we will center the content with a large amount of padding, still giving us a 60rem wide content area.

        

    header img {
        max-width: 40rem; /* limit the width of the JAC logo */
        display: block;
        margin: 0 auto;
    }

    section {
        padding-left: calc(50% - (60rem / 2));
        padding-right: calc(50% - (60rem / 2));

        margin: 2rem; /* optional */
        border-radius: 4rem;  /* optional */
        }

    .earthday .flex-container {
        grid-template-columns: repeat(6, 1fr);  /* 6 columns of 1fr each */
        /* because we are on a bigger screen, we can reduce the size of the icons */
        }

    ## Second Media Query

    Proceed to the next phase: [Designing for desktop scale using CSS Grid](./second-media-query.md)

