 # Class Notes 3.1

 ## Media Query
 
        @media screen and (min-width: 60rem) {

            .wrapper {
                max-width: 60rem; /* 960px */
                margin: 0 auto; /* zero top/bottom, centered left/right */
            }
        } /* always comment closing media query bracket */


## Quiz on floats next class

## HTML URLs on Omnivox

## Finished HTML due end of next class


## HTML picture tag

        <picture>
            <source media="(orientation: portrait)" srcset="img/national-cancer-institute-square-unsplash.jpg">
            
            <source media="(orientation: landscape)" srcset="img/national-cancer-institute-landscape-unsplash.jpg">

            <img src="img/national-cancer-institute-Vb0GY3PWSSM-unsplash.jpg" alt="sample artwork">
            <!-- default img tag for browsers that can't understand the source tag -->
        </picture>













