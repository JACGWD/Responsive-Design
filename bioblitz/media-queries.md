# Controlling Page Layout at Different Viewport Sizes: Media Queries

<blockquote>

1. Media: The technology used to transmit the content.
2. Query: A question.
3. "Media Query": The web browser asks the device's operating system what it is capable of, and displays the page accordingly.

</blockquote>

See: [https://www.w3schools.com/css/css3_mediaqueries_ex.asp](https://www.w3schools.com/css/css3_mediaqueries_ex.asp)

## Examples of How Media Queries Work

### Rules for computer screens

    @media screen {
        h1 {color: red;}
    } 

### Rules for formatting the page when printed    
    
    @media print {
        h1 {color: black;}
    }

### Rules for computer screens that are taller than they are wide    
    
    @media screen and (orientation: portrait) {

        /* use tall background image */

    }

### Rules for computer screens that are narrower than 640px
    
    @media screen and (max-width: 640px) {

        /* display navigation as hamburger menu */
    }


### Rules for computer screens that are wider than 64rem
    
    @media screen and (min-width: 64rem) {

        /* display horizontal navigation menu */
    }

### Rules for computer screens that are narrower than 640px and taller than they are wide
    
    @media screen and (max-width: 640px) and (orientation: landscape) {

        /* use small horizontal background image */
    }