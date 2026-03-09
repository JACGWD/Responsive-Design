# Class Notes 7.1

> ## Important
> Use flexbox for: when, why and how
> 
> Use floats for: who, what and where
>
> **Note:** You only need one media query, placed at the bottom of your stylesheet file.


        @media screen and (min-width: 60rem) {

            /* START FLEXBOX */

            .when .flex-container {
                    display: flex;
                    /* puts elements side-by-side */
                }

            .why .flex-container {
                    display: flex;
                }

            .how .flex-container {
                    display: flex;
                    flex-direction: row-reverse; /* switches content order, picture is second column */
                }

            .when picture {
                width: 50%; /* adjust as necessary */
            }

            .why picture {
                width: 50%; /* adjust as necessary */
            }

            .how picture {
                width: 50%; /* adjust as necessary */
            }



            /* START FLOATS */

            .who .flex-container {
                    display: flow-root;  /* wraps float */
                }

            .what .flex-container {
                    display: flow-root;  
                }

            .where .flex-container {
                    display: flow-root;  
                }

            .who .flex-container picture {
                width: 50%; /* adjust as necessary */
                float: left; /* puts elements side-by-side */
                }

            .what .flex-container picture {
                width: 50%; 
                float: right;  /* switches content order, picture is second column */
                }

            .where .flex-container picture {
                width: 50%; 
                float: left; 
                }



            } /* always comment closing media query */