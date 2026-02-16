# Phase 3: Multi-column Layout Using Media Queries for Larger Devices


## Going from Mobile Scale to Larger Viewports

[Read the overview about media queries here](./media-queries.md)


## Setting elements side-by-side

### Using Flex Box

#### The Basic Alignment

   @media screen and (min-width: 1024px) {
    .when .flex-container {
        display: flex;
        /* puts elements side-by-side */
    }
   } /* always comment closing media query */

or

    @media screen and (min-width: 1024px) {
        .when .flex-container {
            display: flow-root;
            /* wraps float */

            /* alternatively you can use overflow: auto; here
                or add class="clearfix" to the parent 
                element's HTML code */
        }
    
    .when .flex-container picture {
        float: left;
        /* puts elements side-by-side */
        }
    } /* always comment closing media query */


#### Switching the Items Order

    .when .flex-container {
        flex-direction: row-reverse;
        /* places elements in reverse order: last element becomes first */
    }

    or

    .when .flex-container picture {
        float: right;
        /* float to opposite side */
        }

#### Setting Column Width

    .when div,
    .when picture,
    .why div,
    .why picture {
	    flex-basis: 50%;
    }  /* for flexbox */

or
    .when div,
    .when picture,
    .why div,
    .why picture {
	    width: 50%;
    }  /* for floats */



### Using CSS Grid

#### The Basic Alignment & Column Width

     .how .flex-container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        /* two columns: each equal to one fraction of the available space */
    }

#### Switching the Items Order

    .how picture {
        order: 2;
        /* force to go to column 2 */
      }

    .how .flex-container div {
        order: 1;
        /* force to go to column 1 */
    }


## Horizontal & Vertical Centering 

### Using line-height (for a single line of text)

When you have a **single line of text**, you can vertically center it using a line-height equal to the height of the parent element. Then you can use regular text centering.

    footer {
        background-color: #2679d8;
        color: #fff;

        height: 5rem;
        line-height: 5rem;
        /* the **single line** of text is the same height as the box it is in: vertical centering */

        text-align: center;
        /* horizontal centering */
    }


### Using Flex Box

    footer {
        background-color: #2679d8;
        color: #fff;
        height: 5rem;
        
        display: flex;

        align-items: center;
        /* vertical centering */

        justify-content: center;
        /* horizontal centering */
    }


### Flex

Use a media query to make items go side by side using display: flex and display: grid.

See: [https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#setting-elements-side-by-side](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#setting-elements-side-by-side)

### Alternate the position of some items

See: [Flexbox](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#switching-the-items-order) and [CSS Grid](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8b-notes.md#switching-the-items-order-1)

## Step 9: Add CSS background images

See: [Point 6 on this page](https://github.com/JACGWD/Responsive-Design-Winter-2025/blob/main/week-8-notes.md)


## Testing Setup

Use this page to load your page multiple times into iframes of different sizes so you can observe the media queries in action. Requires PHP: use the [wordpressplayground.wordpress-playground VS Code extension](https://marketplace.visualstudio.com/items?itemName=WordPressPlayground.wordpress-playground)

[https://github.com/JACGWD/Responsive-iFrames](https://github.com/JACGWD/Responsive-iFrames)

