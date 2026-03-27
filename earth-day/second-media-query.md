# Designing for desktop scale using CSS Grid

Currently we have:

- Mobile/default view up to 60rem (960px) wide.
- An intermediate view from 60rem to 90rem (1440px) wide.
- An empty media query that starts at 90rem.

## Objective

Use [CSS Grid](https://www.w3schools.com/css/css_grid.asp) to layout the information on the page in a series of rows and columns, similar to print page layout. As you can see in this [screencapture from 960.gs](https://www.960.gs), web site designs can be easily laid out in 12 or 16 columns.

![Screencapture from 960.gs](./img/960gs.png)


### Step-by-Step

1. Everything we will write will be inside the 90rem media query. 

        @media screen and (min-width: 90rem) {

            /* write your css rules here */

        } /* closes media query */


2. Take the time to sketch your layout in terms of columns and rows so you have a visual to follow. You can use [Figma](https://www.figma.com/) for this. **Please create an account using your John Abbott College email address.**

![Screencapture of Figma interface](./img/figma.png)

What you need to find out: 

- How many columns wide will each box be?
- How many rows tall will each box be?
- How many rows will the entire page layout need?


![Figma with Grid](./img/figma-grid.png)


3. Set your browser window width to **exactly 1440px** (90rem).

4. Define the grid in CSS

        main {
            display: grid;
            grid-template-columns: repeat(16, 1fr); /* 16 columns each equal to one fraction of the available space */
            grid-template-rows: repeat(8, auto); /* 5 rows for 5 sections, some double height */
            gap: 2rem;  /* both row and column gap */
        }


Now that we have defined the grid, we can see it in the browser. Note that the child elements of the main tag are each inserted into a column, in the natural flow order. The remaining columns are empty and at the end of the grid.

![CSS grid visible in Microsoft Edge](./img/grid-in-edge.png)

  

5. Note that the page layout will be all out of proportion until all the elements are placed on the grid. So we will temporarily hide all but one section to make it easier to work with:

        .gwd,
        .earthday,
        .logos,
        .giveaway,
        .transplant {
            display: none;
        }


6. Remove the margins and padding inherited from the tablet media query:
   
        section {
            padding-left: unset;
            padding-right: unset;
            margin: 0;
        } 


7. Place an element on the grid

    To place an element on the grid you need to define the starting point: an intersection of a column and a row; and the end point: another intersection of a column and row.


        .macmarket {
            grid-column: 2/13;
            grid-row: 1/1;
            padding: 1rem 8.5% 2rem 8.5%;  /* note that percentages scale better when the window width changes */
            }


8. Remove .earthday from the hidden div list:

        .gwd,
        .logos,
        .giveaway,
        .transplant {
            display: none;
        }


9. Place .earthday on the grid as a right-hand side sidebar.

        .earthday {
             grid-column: 13/16;
             grid-row: 1/8;  /* full height on the grid */
         }


         .earthday .flex-container {
            grid-template-columns: 1fr;
            padding: 1rem;
            margin: 0 auto;
            width: 50%; /* change width to make overall logo column height less */
        }


 10. Remove .gwd from the hidden div list:

        .logos,
        .giveaway,
        .transplant {
           display: none;
        }       


10. Place .gwd on the grid        

        .gwd {
             grid-column: 2/8;
             grid-row: 2/5;
         }

        .gwd h1,
        .gwd h2,
        .gwd .two {
            padding: 1rem;
        }


12. Remove .transplant from the hidden div list:

        .logos,
        .giveaway {
            display: none;
        }


13. Place .transplant on the grid        

        .transplant {
            grid-column: 8/13;
            grid-row: 2/5;
            padding: 1rem;
         }

14. Prepare the .logos for absolute positioning

        .logos {
            position: relative;
        }


15. Position the logos
        .logos .two li {
            position: absolute; /* all logos */
        }

        .logos .two li:nth-child(1) {
            top: 0%;
            left: 0%;
            width: 10rem;
        }

        .logos .two li:nth-child(2) {
             top: 0%;
            left: 0%;
            width: 10rem;
        }

        .logos .two li:nth-child(3) {
             top: 0%;
            left: 0%;
            width: 10rem;
        }

        .logos .two li:nth-child(4) {
            top: 0%;
            left: 0%;
            width: 10rem;
        }

        .logos .two li:nth-child(5) {
             top: 0%;
            left: 0%;
            width: 10rem;
        }
        
