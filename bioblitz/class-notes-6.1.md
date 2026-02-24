# Class Notes, week 6.1

## Be clear what viewport size you are editing

        /* mobile styles here */

        @media screen and (min-width: 60rem) {

            /* desktop styles only go here */

            .wrapper {
                max-width: 60rem;
                margin: 0 auto;
            }


        } /* always comment closing media query bracket */

- Mobile styles come first
- Desktop media query goes **at bottom** of the CSS file


## Objectives of Desktop Design

1. Multiple Page Layout Columns: [Place images and text side by side.](./instructions-3-desktop.md#using-flex-box-and-floats)
   1. who, what and where use floats.
   2. when, why and how use flexbox.
2. Swap left/right position of image and text at regular intervals to entertain the reader's eye.
3. Add decorative ([css background](https://www.w3schools.com/css/css_background.asp)) images now that you have more space.
4. Tweak [font sizes if necessary](./instructions-2-mobile.md#23-pick-your-font-sizes-for-mobile).
5. Add extra imagery using [CSS pseudo-elements](./instructions-3-desktop.md#step-10-adding-extra-decorative-elements)