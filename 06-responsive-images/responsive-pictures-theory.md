# Responsive Pictures

<blockquote>

## Reference Material

See the following W3Schools page for more info about the \<picture> tag: [https://www.w3schools.com/TAGS/tag_picture.asp](https://www.w3schools.com/TAGS/tag_picture.asp)

</blockquote>


## Golden Rule of Responsive CSS: max-width: 100%

The following CSS rule is essential in making images display proportionately to the screen they are displayed on. Essentially it forces the image to be no wider than 100% of its parent, and to maintain a proportional height. 

    img {
        max-width: 100%; 
        height: auto;
        }


## Golden Rule of Responsive HTML: Conditions

<blockquote>

Computers work in **binary** logic. True or false. Black or white. Ones or zeros. 

When building responsiveness into a design, remember that the web browser has to ask the device's operating system a bunch of questions in order to know how to display the page. 

1. Is this a screen, a speaker or a printer?
2. Is it (the screen or printer) a color or black and white?
3. How big is the screen?
4. Is the screen in landscape mode?
5. Is the screen in portrait mode?

</blockquote>

Since **computers can only understand an answer of true or false**, they have to break down complex calculations into a series of yes/no questions. 

1. Is the screen wider than 5192px? **FALSE**
2. Is the screen wider than 4096px? **FALSE**
3. Is the screen wider than 2048px? **FALSE**
4. Is the screen wider than 1920px? **FALSE**
5. Is the screen wider than 1600px? **FALSE**
6. Is the screen wider than 1440px? **FALSE**
7. Is the screen wider than 1280px? **TRUE** ---> Okay, do this...
8. Is the screen wider than 1152px?  (Will not be read because TRUE was found before this line)
9. Is the screen wider than 1024px?
10. Is the screen wider than 960px?
11. Is the screen wider than 800px?
12. Is the screen wider than 640px?
13. Is the screen wider than 480px?
14. Is the screen wider than 400px?
15. Is the screen wider than 320px?
16. Is the screen wider than 240px?

### The order is important!

On a 5000px screen:
Is the screen wider than 240px? **TRUE**
Is the screen wider than 5192px? **TRUE**

On a 320px screen:
Is the screen wider than 5192px? **FALSE**
Is the screen wider than 240px? **TRUE**

## Turning the conditions into code: media queries

<blockquote>

### Media Queries

- Media: The device that displays the information
- Query: A question
- Media Query: The browser asks the device what it's properties and capabilities are.


</blockquote>


### Examples

    <picture>
      <source media="(min-width:650px)" srcset="img_pink_flowers.jpg">
      <source media="(min-width:465px)" srcset="img_white_flower.jpg">
      <img src="img_orange_flowers.jpg" alt="Flowers" style="width:auto;">
    </picture>

## Main Concepts to Remember 

The picture tags works along the same principle as  \<video> and \<audio>: You set up different sources, and the first source that matches the condition is the one that gets used.

### You have to set media queries with the largest width value first! 

### Example 1

    <picture>
      <source media="(min-width:320px)" srcset="img_pink_flowers.jpg">
      <source media="(min-width:800px)" srcset="img_white_flower.jpg">
      <img src="img_orange_flowers.jpg" alt="Flowers">
    </picture>

In this scenario, every device will use the first picture because every device is at least 320px wide. The first media query condition is true so the browser does not go in to read the second rule. 


### Example 2

    <picture>
      <source media="(min-width:800px)" srcset="img_pink_flowers.jpg">
      <source media="(min-width:320px)" srcset="img_white_flower.jpg">
      <img src="img_orange_flowers.jpg" alt="Flowers">
    </picture>

In this scenario, bigger screens will use the 800px rule. But small smartphones will return a false value to the first condition and go on to read the second rule.



