# Google Fonts How To

1. Go to [https://fonts.google.com/](https://fonts.google.com/)
2. Choose a font
3. Click "Get Font" at to right
4. Click "get Embed Code"
5. This part goes at the bottom of \<head> (the third line will be different depending on the fonts you choose):

        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <!-- the above two lines only need to be included once if you are copying/pasting multiple font links -->

        <link href="https://fonts.googleapis.com/css2?family=Boldonse&display=swap" rel="stylesheet">

6. This code goes in your CSS:

        .boldonse-regular {  <-- change the class name to your choice of HTML tag(s) 
            font-family: "Boldonse", system-ui; 
            font-weight: 400;
            font-style: normal;
        }

7. Your final fonts code should look something like this:

        body {   
            font-family: "Boldonse", system-ui; /* this is just an example */
            font-weight: 400;  /* always replace <weight> with a number or keyword */
            font-style: normal;
        }


        h1 { /* Use this font exclusively for the title/branding */
            font-family: "Outfit", sans-serif;  /* this is just an example */
            font-optical-sizing: auto;
            font-weight: 600;  /* always replace <weight> with a number or keyword */
            font-style: normal;
            }


        h2,h3,h4,h5,h6,label,legend {   
            font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;  /* this is just an example */
            font-weight: bold;
            font-style: normal;
        }