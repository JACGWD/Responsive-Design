# Class Notes 7.1

> ## Important
> Use flexbox for: when, why and how
> 
> Use floats for: who, what and where


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
                    display: flow-root;  /* wraps float */
                }

            .where .flex-container {
                    display: flow-root;  /* wraps float */
                }

            .who .flex-container picture {
                width: 50%; /* adjust as necessary */
                float: left; /* puts elements side-by-side */
                }

            .what .flex-container picture {
                width: 50%; /* adjust as necessary */
                float: left; /* puts elements side-by-side */
                }

            .where .flex-container picture {
                width: 50%; /* adjust as necessary */
                float: left; /* puts elements side-by-side */
                }



            } /* always comment closing media query */