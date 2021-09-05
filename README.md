# Responsive Portfolio Website
##

### Responsive Portfolio Website
Responsive Portfolio Website Using Html, Css and JavaScript, With a beautiful user interface. It contains a Header, Home, About, Skills, Qualification, Services, Portfolio, Project in mind, Testimonial, Contact and Footer.
Don't forget to join the channel for more videos like this.

![Resume cv](/preview.png)
# Documentation

## A. PROJECT SETUP & VARIABLE CSS
### index.html
1. Add CSS for webpage styling.
<link rel="stylesheet" href="assets/css/styles.css">

2. Add JavaScript for adding interactive behavior to webpages.
<script src="assets/js/main.js"></script>

3. Add free icon templates using Unicons.
<link rel="stylesheet" href="https://unicons.iconscout.com/release/v4.0.0/css/line.css">

### assets/css/styles.css
4. Add Google font styles.
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600&display=swap');

Under variable css, :root section,
5. Add a header height set in 3rem.
**Note: REM vs EM**
--header-height: 3rem;

6. Below are the 'Colors' css code. Under 'HSL color mode', set the custom properties for color.
**Note: --first-color is a 'Custom Property CSS Variable'. Property names that are prefixed with --, like --example-name, represent custom properties that contain a value that can be used in other declarations using the var() function.
```
/*========== Colors ==========*/
/* Change favorite color */
--hue-color: 250; /*Purple 250 - Green 142 - Blue 230 - Pink 340*/

/* HSL color mode */
--first-color: hsl(var(--hue-color), 69%, 61%); /* #6E57E0 */
--first-color-second: hsl(var(--hue-color), 69%, 61%);
--first-color-alt: hsl(var(--hue-color), 57%, 53%);
--first-color-lighter: hsl(var(--hue-color), 92%, 85%);
--title-color: hsl(var(--hue-color), 8%, 15%);
--text-color: hsl(var(--hue-color), 8%, 45%);
--text-color-light: hsl(var(--hue-color), 8%, 65%);
--input-color: hsl(var(--hue-color), 70%, 96%);
--body-color: hsl(var(--hue-color), 60%, 99%);
--container-color: #FFF;
```

7. Go back to the font you seleced in Google Fonts then under the '@import' radio button copy the code block under 'CSS rules to specify families'. Paste in the 'style.css' file to set the font and typography. Then fill up the values for custom properties for fonts.
```
/*========== Font and typography ==========*/
--body-font: 'Poppins', sans-serif;

/* .5rem = 8px, 1rem = 16px, 1.5rem = 24px ... */
--big-font-size: 2rem;
--h1-font-size: 1.5rem;
--h2-font-size: 1.25rem;
--h3-font-size: 1.125rem;
--normal-font-size: 0.938rem;
--small-font-size: 0.813rem;
--smaller-font-size: 0.75rem;
```

8. Set the font weight.
```
/*========== Font weight ==========*/
--font-medium: 500;
--font-semi-bold: 600;
```

9. Set the margin bottom.
```
/*========== Margenes Bottom ==========*/
/* .25rem = 4px, .5rem = 8px, .75rem = 12px ... */
--mb-0-25: 0.25rem;
--mb-0-5: 0.5rem;
--mb-0-75: 0.75rem;
--mb-1: 1rem;
--mb-1-5: 1.5rem;
--mb-2: 2rem;
--mb-2-5: 2.5rem;
--mb-3: 3rem;
```

10. Set the stack order of the elements.
```
/*========== z index ==========*/
--z-tooltip: 10;
--z-fixed: 100;
--z-modal: 1000;
```

11. Now after finishing the custom properties for the ':root'. Set the settings for large screen responsiveness.
```
@media screen and (min-width: 968px) {
    :root {
        --big-font-size: 3rem;
        --h1-font-size: 2.25rem;
        --h2-font-size: 1.5rem;
        --h3-font-size: 1.25rem;
        --normal-font-size: 1rem;
        --small-font-size: 0.875rem;
        --smaller-font-size: 0.813rem;
    }
}
```

## B. RESET HTML
### assets/css/styles.css
1. Under the 'Base' section, reset the html by adding the ff code.
```
/*==================== BASE ====================*/
*{
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

html{
  scroll-behavior: smooth;
}

body{
  margin: 0 0 var(--header-height) 0;
  font-family: var(--body-font);
  font-size: var(--normal-font-size);
  background-color: var(--body-color);
  color: var(--text-color);
}

h1,h2,h3,h4{
  color: var(--title-color);
  font-weight: var(--font-semi-bold);
}

ul{
  list-style: none;
}

a{
  text-decoration: none;
}

img{
  max-width: 100%;
  height: auto;  
}

```

## C. REUSABLE CSS CLASSES
### assets/css/styles.css
1. Under the 'Reusable CSS Classes' section, add the ff code.
```
/*==================== REUSABLE CSS CLASSES ====================*/
.section{
  padding: 2rem 0 4rem;
}

.section__title{
  font-size: var(--h1-font-size);
}

.section__subtitle{
  display: block;
  font-size: var(--small-font-size);
  margin-bottom: var(--mb-3);
}

.section__title,
.section__subtitle{
  text-align: center;
}
```
