# Week 7b Notes

## Art Review

- Content vs Presentation 
- Not enough content in mocks
- Which images can be background (CSS background image) vs content (HTML picture tag)?


Images for the 5 Ws:

- Who: JAC students 
- What: BioBlitz (what is a bioblitz?)
- Where: JAC/Ste-Anne
- When: Date
- Why: Engage students in crowd-sourced scientific data collection

Get images from Unsplash that illustrate this. 


## Technical Review

- Q: What is the image size?
- Q: What is the text measure width? 

### Notes on Typography

#### The Ideal Line Length
- [https://baymard.com/blog/line-length-readability](https://baymard.com/blog/line-length-readability)

#### Line Length in Web vs Print
- [https://www.viget.com/articles/the-line-length-misconception/](https://www.viget.com/articles/the-line-length-misconception/)

#### Examples of CSS for Limiting Line Length

    p { 
        max-width: 85ch; 
        /* paragraph only */
    } 

    or

    h1,
    h2,
    h3,
    h4,
    h5,
    h6,
    legend,
    label,
    p,
    li { 
        max-width: 100ch; 
        /* most on-screen text */
    }  

## Text Content

<table>
<tbody>
<tr>
<th><strong>Text</strong></th>
<th><strong>Comments</strong></th>
<th>5 Ws</th>
</tr>
<tr>
<td>John Abbott College BioBlitz 2025</td>
<td>Official Title of the Event</td>
<td><strong>What</strong><br />
(general statement)<br />
<br />
Also identifies elements of <strong>Who</strong> and
<strong>When</strong></td>
</tr>
<tr>
<td>A BioBlitz is a communal citizen-science effort to record as many
species as possible, within a designated location and time period, using
the iNaturalist app</td>
<td>&nbsp;</td>
<td><p>What</p>
<p>(detailed statement)</p></td>
</tr>
<tr>
<td>Just make as many iNaturalist observations as possible at JAC</td>
<td>&nbsp;</td>
<td><p>What</p>
<p>(simplified statement to encourage engagement)</p></td>
</tr>
<tr>
<td>The objective is to connect with nature and others, while providing
useful data for scientific biodiversity conservation purposes. </td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td>No sign-up is needed to participate in the BioBlitz. </td>
<td>No sign up for the event<br />
<br />
(But you need an iNaturalist account for uploading photos with the
app.)</td>
<td>&nbsp;</td>
</tr>
<tr>
<td>April 25-28 2025</td>
<td>Tentative dates (based on last year’s event)</td>
<td>When</td>
</tr>
<tr>
<td>John Abbott College campus &amp; surrounding areas</td>
<td>&nbsp;</td>
<td>Where</td>
</tr>
<tr>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td>iNaturalist</td>
<td>Client Organization (beneficiary)</td>
<td>&nbsp;</td>
</tr>
<tr>
<td><p>Connect with Nature</p>
<p>Explore and share your observations from the natural world.</p></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td><p><strong>Download the Naturalist App</strong><br />
Works On All Your Devices</p>
<p>Install our mobile app so you can always observe, even without cell
reception or wifi.<br />
<br />
<a
href="https://play.google.com/store/apps/details?id=org.inaturalist.android">https://play.google.com/store/apps/details?id=org.inaturalist.android</a><br />
</p>
<p><a
href="https://itunes.apple.com/us/app/inaturalist/id421397028?mt=8">https://itunes.apple.com/us/app/inaturalist/id421397028?mt=8</a></p>

<p>You must create an account at iNaturalist</p></td>
<td>Methodology</td>
<td>How</td>
</tr>
<tr>
<td><p>How It Works</p>
<p>1. Record your observations</p>
<p>2. Share with fellow naturalists</p>
<p>3. Discuss your findings</p></td>
<td>&nbsp;</td>
<td>How<br />
<br />
(simplified statement to encourage engagement)</td>
</tr>
<tr>
<td><p>Contribute to Science<br />
</p>
<p>Every observation can contribute to biodiversity science, from the
rarest butterfly to the most common backyard weed. We share your
findings with scientific data repositories like the <a
href="http://gbif.org/">Global Biodiversity Information Facility</a>
(http://gbif.org/) to help scientists find and use your data. All you
have to do is observe. </p></td>
<td>&nbsp;</td>
<td>Why</td>
</tr>
<tr>
<td><p>John Abbott College Campus Biodiversity Network</p>
<p>Observations will appear on this page:</p>
<p><br />
https://inaturalist.ca/projects/john-abbott-college-campus-biodiversity-network</p></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
</tbody>
</table>


## Assignment: Mobile

1. Create a standard html page
2. Add style tag inside head
3. Add multiple images using orientation media query and 1x + 2x resolutions. Image width is defined by column width in Figma. 
4. Remember that 2x images must be saved from same size or bigger images. **Not scaled up from smaller sizes.** 
5. Wrap elements (picture + picture, picture + text, etc) that will be side by side on larger screens inside a div. Use a "flex-container" class. 

### Fonts

- Find Legal typefaces
- Adobe
- Google

#### Three fonts: Brand, headers, body
- Find longest title, choose h1 size accordingly for mobile
- Use type scale to find intermediates

### Color palette

Define color variables:

#### header

- Header background color
- Header text color
- Header anchor LoVeHA

#### main

- Main background color
- Main text color
- Main anchor LoVeHA

#### footer

- Footer background color
- Footer text color
- Footer anchor LoVeHA

#### LoVeHA Rule Colors & Styles

    header a:link {}
    header a:visited  {}
    header a:hover  {}
    header a:active {}

    main a:link  {}
    main a:visited  {}
    main a:hover  {}
    main a:active  {}

    footer a:hover  {}
    footer a:active  {}
    footer a:hover  {}
    footer a:active  {}

### Background Images

1. Place full resolution images in Figma
2. Export resized/designed elements from Figma as 1x and 2x
3. Add as:

        header {
            background-image: url(css/img/bg.jpg); /* 1x version */
            background-repeat: no-repeat;
            background-size: cover;
        }

        @media (min-resolution: 2x) {

        header {
            background-image: url(css/img/bg2x.jpg); /* 2x version */
            /* do not repeat css properties that don’t change */
        }

        } /* always comment closing media query */


## Configuring SSH FS

[Instructions to how to configure SSH FS can be found on this GitHub repo](https://github.com/JACGWD/configuring-sshfs)


## Testing Setup

Use this page to load your page multiple times into iframes of different sizes so you can observe the media queries in action. Requires PHP: use the [wordpressplayground.wordpress-playground VS Code extension](https://marketplace.visualstudio.com/items?itemName=WordPressPlayground.wordpress-playground)

[https://github.com/JACGWD/Responsive-iFrames](https://github.com/JACGWD/Responsive-iFrames)

