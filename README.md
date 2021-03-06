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

## D. LAYOUT
### assets/css/styles.css
1. Under the 'Layout' section, add the ff code.
```
/*==================== LAYOUT ====================*/
.container{
  max-width: 768px;
  margin-left: var(--mb-1-5);
  margin-right: var(--mb-1-5);
}

.grid{
  display: grid;
  gap: 1.5rem;
}
```

## E. HEADER & NAV MENU
### index.html
1. Under the 'Header' section in the body tag, add the ff code.
```
<!--==================== HEADER ====================-->
<header class="header" id="header">
  <nav class="nav container">
    <a href="#" class="nav__logo">Steven</a>

    <div class="nav__menu" id="nav-menu">
      <ul class="nav__list grid">
        <li class="nav__item">
          <a href="#" class="nav__link">

          </a>
          <a href="#" class="nav__link">

          </a>
          <a href="#" class="nav__link">

          </a>
          <a href="#" class="nav__link">

          </a>
          <a href="#" class="nav__link">

          </a>
        </li>
      </ul>
    </div>
  </nav>
</header>
```
2. Go to Iconscout then add icons for the navbar.
Search 'home' first then copy the font code to the 1st list element.
Add a space after the icon before the anchor text.
Add URL in the href.
```
<!--==================== HEADER ====================-->
<header class="header" id="header">
  <nav class="nav container">
    <a href="#" class="nav__logo">Steven</a>

    <div class="nav__menu" id="nav-menu">
      <ul class="nav__list grid">
        <li class="nav__item">
          <a href="#home" class="nav__link">
            <i class="uil uil-estate"></i> Home
          </a
        </li>
        <li class="nav__item">
          <a href="#" class="nav__link">

          </a>
        </li>
        <li class="nav__item">
          <a href="#" class="nav__link">

          </a>
        </li>
        <li class="nav__item">
          <a href="#" class="nav__link">

          </a>
        </li>
        <li class="nav__item">
          <a href="#" class="nav__link">

          </a>
        </li>
        <li class="nav__item">
          <a href="#" class="nav__link">

          </a>
        </li>
      </ul>
    </div>
  </nav>
</header>
```
3. Do the same for the ff icons: About, Skills, Services, Portfolio, Contact Me.
```
<!--==================== HEADER ====================-->
<header class="header" id="header">
  <nav class="nav container">
    <a href="#" class="nav__logo">Steven</a>

    <div class="nav__menu" id="nav-menu">
      <ul class="nav__list grid">
        <li class="nav__item">
          <a href="#home" class="nav__link">
            <i class="uil uil-estate"></i> Home
          </a>
        </li>
        <li class="nav__item">
          <a href="#about" class="nav__link">
            <i class="uil uil-user"></i> About
          </a>
        </li>
        <li class="nav__item">
          <a href="#skills" class="nav__link">
            <i class="uil uil-file-alt"></i> Skills
          </a>
        </li>
        <li class="nav__item">
          <a href="#services" class="nav__link">
            <i class="uil uil-briefcase-alt"></i> Services
          </a>
        </li>
        <li class="nav__item">
          <a href="#portfolio" class="nav__link">
            <i class="uil uil-scenery"></i> Portfolio
          </a>
        </li>
        <li class="nav__item">
          <a href="#contact" class="nav__link">
            <i class="uil uil-message"></i> Contact Me
          </a>
        </li>
      </ul>
    </div>
  </nav>
</header>
```

4. Add a nav__close and nav__toggle from Iconscout in the header.
```
<!--==================== HEADER ====================-->
<header class="header" id="header">
  <nav class="nav container">
    <a href="#" class="nav__logo">Steven</a>

    <div class="nav__menu" id="nav-menu">
      <ul class="nav__list grid">
        <li class="nav__item">
          <a href="#home" class="nav__link">
            <i class="uil uil-estate"></i> Home
          </a>
        </li>
        <li class="nav__item">
          <a href="#about" class="nav__link">
            <i class="uil uil-user"></i> About
          </a>
        </li>
        <li class="nav__item">
          <a href="#skills" class="nav__link">
            <i class="uil uil-file-alt"></i> Skills
          </a>
        </li>
        <li class="nav__item">
          <a href="#services" class="nav__link">
            <i class="uil uil-briefcase-alt"></i> Services
          </a>
        </li>
        <li class="nav__item">
          <a href="#portfolio" class="nav__link">
            <i class="uil uil-scenery"></i> Portfolio
          </a>
        </li>
        <li class="nav__item">
          <a href="#contact" class="nav__link">
            <i class="uil uil-message"></i> Contact Me
          </a>
        </li>
      </ul>
      <i class="uil uil-times nav__close" id="nav-close"></i>
    </div>

    <div class="nav__">
      <div class="nav__toggle" id="nav-toggle">
        <i class="uil uil-apps"></i>
      </div>
    </div>
  </nav>
</header>
```

### assets/css/styles.css
1. Under the 'Layouts' section, add the ff code.
```
.header{
  width: 100%;
  position: fixed;
  bottom: 0;
  left: 0;
  z-index: var(--z-fixed);
  background-color: var(--body-color);
}
```

Preview.
![](/readme-img/Header & Nav Menu1.png)

2. Under the 'Nav' section, add the ff code.
```
.nav{
  max-width: 968px;
  height: var(--header-height);
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

Preview.
![](/readme-img/Header & Nav Menu2.png)

3. Now we'll change the color and the font weight of 'Steven' and the nav__toggle.
Add the ff code next.
```
.nav__logo,
.nav_toggle{
  color: var(--title-color);
  font-weight: var(--font-medium);
}
```

Preview.
![](/readme-img/Header & Nav Menu3.png)

4. Now we'll add a hover effect of color change in the 'Steven' logo.
```
.nav__logo:hover{
  color: var(--first-color);  
}
```

Preview.
![](/readme-img/Header & Nav Menu4.png)

5. Now we'll add a hover effect of color change in the nav toggle.
```
.nav_toggle{
  font-size: 1.1rem;
  cursor: pointer;
}

.nav__toggle:hover{
  color: var(--first-color);

}
```

6. Now we'll add code for responsiveness.
```
@media screen and (max-width: 767px){
  .nav__menu{
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    background-color: var(--body-color);
    padding: 2rem 1.5rem 4rem;
    box-shadow: 0 -1px 4px rgba(0,0,0,0.15);
    border-radius: 1.5rem 1.5rem 0 0;
    transition: 0.3s;
  }
}
```

Preview.
![](/readme-img/Header & Nav Menu5.png)

7. Next we're going to apply a 3-column grid in nav bar.
```
.nav__list{
  grid-template-columns: repeat(3,1fr);
  gap: 2rem;
}
```

Preview.
![](/readme-img/Header & Nav Menu6.png)

8. Now we'll add a hover effect of color change in the nav links.
```
.nav__link{
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: var(--small-font-size);
  color: var(--title-color);
  font-weight: var(--font-medium);
}

.nav__link:hover{
  color: var(--first-color);
}
```

Preview.
![](/readme-img/Header & Nav Menu7.png)

9. Next we will adjust the font-size of the icons and the font color of the nav close button.
```
.nav__icon{
  font-size: 1.2rem;
}

.nav__close{
  position: absolute;
  right: 1.3rem;
  bottom: 0.5rem;
  font-size: 1.5rem;
  cursor: pointer;
  color: var(--first-color);
}

.nav__close:hover{
  color: var(--first-color-alt);
}
```

10. Now it's time to add an effect to have the nav bar pop up from bottom (for small screens).
Change the 'bottom' parameter in the nav section under responsiveness code block.
```
@media screen and (max-width: 767px){
  .nav__menu{
    position: fixed;
    bottom: -100%;
    left: 0;
    width: 100%;
    background-color: var(--body-color);
    padding: 2rem 1.5rem 4rem;
    box-shadow: 0 -1px 4px rgba(0,0,0,0.15);
    border-radius: 1.5rem 1.5rem 0 0;
    transition: 0.3s;
  }
}
```

Preview.
![](/readme-img/Header & Nav Menu8.png)

### assets/js/main.js
1. Now let's add our first javascript.
```
/*==================== MENU SHOW Y HIDDEN ====================*/
const navMenu = document.getElementById('nav-menu'),
      navToggle = document.getElementById('nav-toggle')
      navClose = document.getElementById('nav-close')

/*===== MENU SHOW =====*/
/* Validate if constant exists */
if(navToggle){
  navToggle.addEventListener('click', ()=>{
    navMenu.classList.add('show-menu')
  })
}
```

### assets/css/styles.css
11. After adding the new javascript code, let's style the show menu.
```
/* show menu */
.show-menu{
  bottom: 0;
}
```

Let's refresh the webpage to seee the changes. As you can see if we click the nav toggle a menu of links will show up.
Take note that the nav close is not working yet when you try clicking it to close the menu.

### assets/js/main.js
2. Let's add a close feature in our show menu.
```
/*===== MENU HIDDEN =====*/
/* Validate if constant exists */
if(navClose){
  navClose.addEventListener('click', ()=>{
    navMenu.classList.remove('show-menu')
  })
}
```

3. Next we add a similar feature when we click the links. This JavaScript will close the menu each time you click a link.
```
/*==================== REMOVE MENU MOBILE ====================*/
const navLink = document.querySelectorAll('.nav__link')

function linkAction(){
  const navMenu = document.getElementById('nav-menu')
  // When we click on each nav__link, we remove the show-menu class
  navMenu.classList.remove('show-menu')
}
navLink.forEach(n => n.addEventListener('click', linkAction))
```

## F. HOME
### index.html
1. Let's start creating our homepage by adding social media links.
Under the MAIN >> HOME, add the ff code.
```
<!--==================== HOME ====================-->
<section class="home section" id="home">
    <div class="home__container container grid">
      <div class="home__content grid">
        <div class="home__social">
          <a href="https://www.linkedin.com/" target="_blank" class="home__social-icon">
            <i class="uil uil-linkedin-alt"></i>
          </a>

          <a href="https://www.dribble.com/" target="_blank"class="home__social-icon">
            <i class="uil uil-dribbble"></i>
          </a>

          <a href="https://github.com/" target="_blank" class="home__social-icon">
            <i class="uil uil-github-alt"></i>
          </a>
        </div>


      </div>
    </div>
</section>
```

Preview.
![](/readme-img/Home1.png)

2. Next we add a blob. Open /assets/img/blob.svg and copy the code.
Create a new div inside HOME >> MAIN section and paste the svg code.
Note that we have a profile image without bg saved in the assets.
```
<!--==================== HOME ====================-->
<section class="home section" id="home">
    <div class="home__container container grid">
      <div class="home__content grid">
        <div class="home__social">
          <a href="https://www.linkedin.com/" target="_blank" class="home__social-icon">
            <i class="uil uil-linkedin-alt"></i>
          </a>

          <a href="https://www.dribble.com/" target="_blank"class="home__social-icon">
            <i class="uil uil-dribbble"></i>
          </a>

          <a href="https://github.com/" target="_blank" class="home__social-icon">
            <i class="uil uil-github-alt"></i>
          </a>
        </div>

        <div class="home__img">
          <svg class="home__blob" viewBox="0 0 200 187" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
              <mask id="mask0" mask-type="alpha">
                  <path d="M190.312 36.4879C206.582 62.1187 201.309 102.826 182.328 134.186C163.346 165.547
                  130.807 187.559 100.226 186.353C69.6454 185.297 41.0228 161.023 21.7403 129.362C2.45775
                  97.8511 -7.48481 59.1033 6.67581 34.5279C20.9871 10.1032 59.7028 -0.149132 97.9666
                  0.00163737C136.23 0.303176 174.193 10.857 190.312 36.4879Z"/>
              </mask>
              <g mask="url(#mask0)">
                  <path d="M190.312 36.4879C206.582 62.1187 201.309 102.826 182.328 134.186C163.346
                  165.547 130.807 187.559 100.226 186.353C69.6454 185.297 41.0228 161.023 21.7403
                  129.362C2.45775 97.8511 -7.48481 59.1033 6.67581 34.5279C20.9871 10.1032 59.7028
                  -0.149132 97.9666 0.00163737C136.23 0.303176 174.193 10.857 190.312 36.4879Z"/>

                  <image class="home__blob-img" href="assets/img/profile.png"/>
              </g>
          </svg>
        </div>
      </div>
    </div>
</section>
```

Preview.
![](/readme-img/Home2.png)

3. Let's add a profile tagline.
```
<!--==================== HOME ====================-->
<section class="home section" id="home">
    <div class="home__container container grid">
      <div class="home__content grid">
        <div class="home__social">
          <a href="https://www.linkedin.com/" target="_blank" class="home__social-icon">
            <i class="uil uil-linkedin-alt"></i>
          </a>

          <a href="https://www.dribble.com/" target="_blank"class="home__social-icon">
            <i class="uil uil-dribbble"></i>
          </a>

          <a href="https://github.com/" target="_blank" class="home__social-icon">
            <i class="uil uil-github-alt"></i>
          </a>
        </div>

        <div class="home__img">
          <svg class="home__blob" viewBox="0 0 200 187" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
              <mask id="mask0" mask-type="alpha">
                  <path d="M190.312 36.4879C206.582 62.1187 201.309 102.826 182.328 134.186C163.346 165.547
                  130.807 187.559 100.226 186.353C69.6454 185.297 41.0228 161.023 21.7403 129.362C2.45775
                  97.8511 -7.48481 59.1033 6.67581 34.5279C20.9871 10.1032 59.7028 -0.149132 97.9666
                  0.00163737C136.23 0.303176 174.193 10.857 190.312 36.4879Z"/>
              </mask>
              <g mask="url(#mask0)">
                  <path d="M190.312 36.4879C206.582 62.1187 201.309 102.826 182.328 134.186C163.346
                  165.547 130.807 187.559 100.226 186.353C69.6454 185.297 41.0228 161.023 21.7403
                  129.362C2.45775 97.8511 -7.48481 59.1033 6.67581 34.5279C20.9871 10.1032 59.7028
                  -0.149132 97.9666 0.00163737C136.23 0.303176 174.193 10.857 190.312 36.4879Z"/>

                  <image class="home__blob-img" href="assets/img/profile.png"/>
              </g>
          </svg>
        </div>

        <div class="home__data">
          <h1 class="home__title">Hi, I'm Steven</h1>
          <h3 class="home__subtitle">Fullstack RPA Developer</h3>
          <p class="home__description">Building quality websites and helping companies automate tasks.</p>
          <a href="#contact" class="button button--flex">
            Contact Me <i class="uil uil-message button__icon"></i>
          </a>
        </div>
      </div>
    </div>
</section>
```

Preview.
![](/readme-img/Home3.png)

4. Let's add a scroll down icon below the tagline.
```
<!--==================== HOME ====================-->
<section class="home section" id="home">
    <div class="home__container container grid">
      <div class="home__content grid">
        <div class="home__social">
          <a href="https://www.linkedin.com/" target="_blank" class="home__social-icon">
            <i class="uil uil-linkedin-alt"></i>
          </a>

          <a href="https://www.dribble.com/" target="_blank"class="home__social-icon">
            <i class="uil uil-dribbble"></i>
          </a>

          <a href="https://github.com/" target="_blank" class="home__social-icon">
            <i class="uil uil-github-alt"></i>
          </a>
        </div>

        <div class="home__img">
          <svg class="home__blob" viewBox="0 0 200 187" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
              <mask id="mask0" mask-type="alpha">
                  <path d="M190.312 36.4879C206.582 62.1187 201.309 102.826 182.328 134.186C163.346 165.547
                  130.807 187.559 100.226 186.353C69.6454 185.297 41.0228 161.023 21.7403 129.362C2.45775
                  97.8511 -7.48481 59.1033 6.67581 34.5279C20.9871 10.1032 59.7028 -0.149132 97.9666
                  0.00163737C136.23 0.303176 174.193 10.857 190.312 36.4879Z"/>
              </mask>
              <g mask="url(#mask0)">
                  <path d="M190.312 36.4879C206.582 62.1187 201.309 102.826 182.328 134.186C163.346
                  165.547 130.807 187.559 100.226 186.353C69.6454 185.297 41.0228 161.023 21.7403
                  129.362C2.45775 97.8511 -7.48481 59.1033 6.67581 34.5279C20.9871 10.1032 59.7028
                  -0.149132 97.9666 0.00163737C136.23 0.303176 174.193 10.857 190.312 36.4879Z"/>

                  <image class="home__blob-img" href="assets/img/profile.png"/>
              </g>
          </svg>
        </div>

        <div class="home__data">
          <h1 class="home__title">Hi, I'm Steven</h1>
          <h3 class="home__subtitle">Fullstack RPA Developer</h3>
          <p class="home__description">Building quality websites and helping companies automate tasks.</p>
          <a href="#contact" class="button button--flex">
            Contact Me <i class="uil uil-message button__icon"></i>
          </a>
        </div>
      </div>

      <div class="home__scroll">
        <a href="#about" class="home__scroll-button button--flex">
          <i class="uil uil-mouse-alt home__scroll-mouse"></i>
          <span class="home__scroll-name">Scroll down</span>
          <i class="uil uil-arrow-down home__scroll-arrow"></i>
        </a>
      </div>
    </div>
</section>
```

Preview.
![](/readme-img/Home4.png)

### assets/css/styles.css
1. Let's change the orientation of social media icons in home and a change color hover effect.
```
/*==================== HOME ====================*/
.home__container{
  gap: 1rem;
}

.home__content{
  grid-template-columns: 0.5fr 3fr;
  padding-top: 3.5rem;
  align-items: center;
}

.home__social{
  display: grid;
  grid-template-columns: max-content;
  row-gap: 1rem;
}

.home__social-icon{
  font-size: 1.25rem;
  color: var(--first-color);
}

.home__social-icon:hover{
  color: var(--first-color-alt);
}
```

Preview.
![](/readme-img/Home5.png)

2. Let's change the color of the blob.
```
/*==================== HOME ====================*/
.home__container{
  gap: 1rem;
}

.home__content{
  grid-template-columns: 0.5fr 3fr;
  padding-top: 3.5rem;
  align-items: center;
}

.home__social{
  display: grid;
  grid-template-columns: max-content;
  row-gap: 1rem;
}

.home__social-icon{
  font-size: 1.25rem;
  color: var(--first-color);
}

.home__social-icon:hover{
  color: var(--first-color-alt);
}

.home__blob{
  width: 200px;
  fill: var(--first-color);
}
```
Preview.
![](/readme-img/Home6.png)

3. Next we make our profile image smaller so it will fit our blob.
```
/*==================== HOME ====================*/
.home__container{
  gap: 1rem;
}

.home__content{
  grid-template-columns: 0.5fr 3fr;
  padding-top: 3.5rem;
  align-items: center;
}

.home__social{
  display: grid;
  grid-template-columns: max-content;
  row-gap: 1rem;
}

.home__social-icon{
  font-size: 1.25rem;
  color: var(--first-color);
}

.home__social-icon:hover{
  color: var(--first-color-alt);
}

.home__blob{
  width: 200px;
  fill: var(--first-color);
}

.home__blob-img{
  width: 170px;  
}
```

Preview.
![](/readme-img/Home7.png)

### index.html
5. Now we adjust the alignment of the profile image inside the blob so it will fit nicely.
Go to class home__blob-img and add an x and y positions.
```
<!--==================== HOME ====================-->
<section class="home section" id="home">
    <div class="home__container container grid">
      <div class="home__content grid">
        <div class="home__social">
          <a href="https://www.linkedin.com/" target="_blank" class="home__social-icon">
            <i class="uil uil-linkedin-alt"></i>
          </a>

          <a href="https://www.dribble.com/" target="_blank"class="home__social-icon">
            <i class="uil uil-dribbble"></i>
          </a>

          <a href="https://github.com/" target="_blank" class="home__social-icon">
            <i class="uil uil-github-alt"></i>
          </a>
        </div>

        <div class="home__img">
          <svg class="home__blob" viewBox="0 0 200 187" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
              <mask id="mask0" mask-type="alpha">
                  <path d="M190.312 36.4879C206.582 62.1187 201.309 102.826 182.328 134.186C163.346 165.547
                  130.807 187.559 100.226 186.353C69.6454 185.297 41.0228 161.023 21.7403 129.362C2.45775
                  97.8511 -7.48481 59.1033 6.67581 34.5279C20.9871 10.1032 59.7028 -0.149132 97.9666
                  0.00163737C136.23 0.303176 174.193 10.857 190.312 36.4879Z"/>
              </mask>
              <g mask="url(#mask0)">
                  <path d="M190.312 36.4879C206.582 62.1187 201.309 102.826 182.328 134.186C163.346
                  165.547 130.807 187.559 100.226 186.353C69.6454 185.297 41.0228 161.023 21.7403
                  129.362C2.45775 97.8511 -7.48481 59.1033 6.67581 34.5279C20.9871 10.1032 59.7028
                  -0.149132 97.9666 0.00163737C136.23 0.303176 174.193 10.857 190.312 36.4879Z"/>

                  <image class="home__blob-img" x='12' y='18' href="assets/img/profile.png"/>
              </g>
          </svg>
        </div>

        <div class="home__data">
          <h1 class="home__title">Hi, I'm Steven</h1>
          <h3 class="home__subtitle">Fullstack RPA Developer</h3>
          <p class="home__description">Building quality websites and helping companies automate tasks.</p>
          <a href="#contact" class="button button--flex">
            Contact Me <i class="uil uil-message button__icon"></i>
          </a>
        </div>
      </div>

      <div class="home__scroll">
        <a href="#about" class="home__scroll-button button--flex">
          <i class="uil uil-mouse-alt home__scroll-mouse"></i>
          <span class="home__scroll-name">Scroll down</span>
          <i class="uil uil-arrow-down home__scroll-arrow"></i>
        </a>
      </div>
    </div>
</section>
```

Preview.
![](/readme-img/Home8.png)

### assets/css/styles.css
4. We're going to fix the alignment of the description for our profile image.
We add a setting for '.home__data'.
```
/*==================== HOME ====================*/
.home__container{
  gap: 1rem;
}

.home__content{
  grid-template-columns: 0.5fr 3fr;
  padding-top: 3.5rem;
  align-items: center;
}

.home__social{
  display: grid;
  grid-template-columns: max-content;
  row-gap: 1rem;
}

.home__social-icon{
  font-size: 1.25rem;
  color: var(--first-color);
}

.home__social-icon:hover{
  color: var(--first-color-alt);
}

.home__blob{
  width: 200px;
  fill: var(--first-color);
}

.home__blob-img{
  width: 170px;
}

.home__data{
  grid-column: 1/3;
}
```

Preview.
![](/readme-img/Home9.png)

5. Next we're going to apply formatting to the text for classes: '.home__title', '.home__subtitle'.
```
.home__container{
  gap: 1rem;
}

.home__content{
  grid-template-columns: 0.5fr 3fr;
  padding-top: 3.5rem;
  align-items: center;
}

.home__social{
  display: grid;
  grid-template-columns: max-content;
  row-gap: 1rem;
}

.home__social-icon{
  font-size: 1.25rem;
  color: var(--first-color);
}

.home__social-icon:hover{
  color: var(--first-color-alt);
}

.home__blob{
  width: 200px;
  fill: var(--first-color);
}

.home__blob-img{
  width: 170px;
}

.home__data{
  grid-column: 1/3;
}

.home__title{
  font-size: var(--big-font-size);
}

.home__subtitle{
  font-size: var(--h3-font-size);
  color: var(--text-color);
  font-weight: var(--font-medium);
  margin-bottom: var(--mb-0-75);
}
```

Preview.
![](/readme-img/Home10.png)

6. Next we set a margin bottom for the text for '.home__description' class and some formatting in the scroll button '.home__scroll'.
```
/*==================== HOME ====================*/
.home__container{
  gap: 1rem;
}

.home__content{
  grid-template-columns: 0.5fr 3fr;
  padding-top: 3.5rem;
  align-items: center;
}

.home__social{
  display: grid;
  grid-template-columns: max-content;
  row-gap: 1rem;
}

.home__social-icon{
  font-size: 1.25rem;
  color: var(--first-color);
}

.home__social-icon:hover{
  color: var(--first-color-alt);
}

.home__blob{
  width: 200px;
  fill: var(--first-color);
}

.home__blob-img{
  width: 170px;
}

.home__data{
  grid-column: 1/3;
}

.home__title{
  font-size: var(--big-font-size);
}

.home__subtitle{
  font-size: var(--h3-font-size);
  color: var(--text-color);
  font-weight: var(--font-medium);
  margin-bottom: var(--mb-0-75);
}

.home__description{
  margin-bottom: var(--mb-2);
}

.home__scroll{
  /* display: none; */
}

.home__scroll-button{
  color: var(--first-color);
  transition: 0.3s;
}

.home__scroll-button:hover{
  transform: translateY(0.25rem);
}

.home__scroll-mouse{
  font-size: 2rem;
}

.home__scroll-name{
  font-size: var(--small-font-size);
  color: var(--title-color);
  font-weight: var(--font-medium);
  margin-right: var(--mb-0-25);
}

.home__scroll-arrow{
  font-size: 1.25rem;
}
```

Preview.
![](/readme-img/Home11.png)

## G. BUTTONS
### assets/css/styles.css
1. Now we're going to style our 'Contact Me' button.
```
/*==================== BUTTONS ====================*/
.button{
  display: inline-block;
  background-color: var(--first-color);
  color: #FFF;
  padding: 1rem;
  border-radius: 0.5rem;
  font-weight: var(--font-medium);
}
```

Preview.
![](/readme-img/Buttons1.png)

2. Next we add a hover effect and fix the text alignment inside the button.
```
/*==================== BUTTONS ====================*/
.button{
  display: inline-block;
  background-color: var(--first-color);
  color: #FFF;
  padding: 1rem;
  border-radius: 0.5rem;
  font-weight: var(--font-medium);
}

.button:hover{
  background-color: var(--first-color-alt);
}

.button__icon{
  font-size: 1.25rem;
  margin-left: var(--mb-0-5);
  transition: 0.3s;
}

.button--flex{
  display: inline-flex;
  align-items: center;
}
```

## H. ABOUT
### index.html
1. Now we're creating an ABOUT section.
```
<!--==================== ABOUT ====================-->
<section class="about section" id="about">
  <h2 class="section__title">About Me</h2>
  <span class="section__subtitle">My Introduction</span>
  <div class="about__container container grid">
    <img src="assets/img/about.png" alt="" class="about__img">
    <div class="about__data">
      <p class="about__description">
        Worked as data and reports analyst for four years
        with experience in website and microapps development and
        building workflows automation for banking-BPO, ecommerce and startup companies.
      </p>

      <div class="about__info">
        <div>
          <span class="about__info-title">08+</span>
          <span class="about__info-name">Years <br> experience</span>
        </div>

        <div>
          <span class="about__info-title">20+</span>
          <span class="about__info-name">Completed <br> projects</span>
        </div>

        <div>
          <span class="about__info-title">05+</span>
          <span class="about__info-name">Companies <br> worked</span>
        </div>
      </div>


    </div>
  </div>
</section>
```

Preview.
![](/readme-img/About1.png)

2. Insert a download button for the resume.
```
<!--==================== ABOUT ====================-->
<section class="about section" id="about">
  <h2 class="section__title">About Me</h2>
  <span class="section__subtitle">My Introduction</span>
  <div class="about__container container grid">
    <img src="assets/img/about.png" alt="" class="about__img">
    <div class="about__data">
      <p class="about__description">
        Worked as data and reports analyst for four years
        with experience in website and microapps development and
        building workflows automation for banking-BPO, ecommerce and startup companies.
      </p>

      <div class="about__info">
        <div>
          <span class="about__info-title">08+</span>
          <span class="about__info-name">Years <br> experience</span>
        </div>

        <div>
          <span class="about__info-title">20+</span>
          <span class="about__info-name">Completed <br> projects</span>
        </div>

        <div>
          <span class="about__info-title">05+</span>
          <span class="about__info-name">Companies <br> worked</span>
        </div>
      </div>

      <div class="about__buttons">
        <a download="" href="assets/pdf/resume-cv.pdf" class="button button--flex">
          Download Resume<i class="uil uil-download-alt button__icon"></i>
        </a>
      </div>
    </div>
  </div>
</section>
```

Preview.
![](/readme-img/About2.png)

### assets/css/styles.css
1. Now we will be applying some styling in the 'about' image and description.
```
/*==================== ABOUT ====================*/
.about__img{
  width: 200px;
  border-radius: 0.5rem;
  justify-self: center;
  align-self: center;
}

.about__description{
  text-align: center;
  margin-bottom: var(--mb-2-5);
}
```

2. Next we're going to change the styling for the 'about' info.
```
/*==================== ABOUT ====================*/
.about__img{
  width: 200px;
  border-radius: 0.5rem;
  justify-self: center;
  align-self: center;
}

.about__description{
  text-align: center;
  margin-bottom: var(--mb-2-5);
}

.about__info{
  display: flex;
  justify-content: space-evenly;
  margin-bottom: var(--mb-2-5);
}

.about__info-title{
  font-size: var(--h2-font-size);
  font-weight: var(--font-semi-bold);
  color: var(--title-color);
}

.about__info-name{
  font-size: var(--smaller-font-size);
}

.about__info-title,
.about__info-name{
  display: block;
  text-align: center;
}
```

Preview.
![](/readme-img/About3.png)

3. Next we center the 'Download Resume' button.
```
/*==================== ABOUT ====================*/
.about__img{
  width: 200px;
  border-radius: 0.5rem;
  justify-self: center;
  align-self: center;
}

.about__description{
  text-align: center;
  margin-bottom: var(--mb-2-5);
}

.about__info{
  display: flex;
  justify-content: space-evenly;
  margin-bottom: var(--mb-2-5);
}

.about__info-title{
  font-size: var(--h2-font-size);
  font-weight: var(--font-semi-bold);
  color: var(--title-color);
}

.about__info-name{
  font-size: var(--smaller-font-size);
}

.about__info-title,
.about__info-name{
  display: block;
  text-align: center;
}

.about__buttons{
  display: flex;
  justify-content: center;
}
```

Preview.
![](/readme-img/About4.png)

## I. SKILLS
### index.html
1. Now we're going to add a 'Skills' section.
```
<!--==================== SKILLS ====================-->
<section class="skills section" id="skills">
  <h2 class="section__title">Skills</h2>
  <span class="section__subtitle">My Technical Level</span>
</section>
```

Preview.
![](/readme-img/Skills1.png)

2. Let's add our first skill.
```
<!--==================== SKILLS ====================-->
<section class="skills section" id="skills">
  <h2 class="section__title">Skills</h2>
  <span class="section__subtitle">My Technical Level</span>

  <div class="skills__container container grid">
    <div>
      <!--==================== SKILLS 1 ====================-->
      <div class="skills__content">
        <div class="skills__header">
          <i class="uil uil-brackets-curly skills__icon"></i>

          <div>
            <h1 class="skills__title">Frontend Developer</h1>
            <span class="skills__subtitle">More than 4 years</span>
          </div>

            <i class="uil uil-angle-down skills__arrow"></i>
        </div>
      </div>
    </div>
  </div>
</section>
```

3. Next we add the languages and technologies we know.
```
<!--==================== SKILLS ====================-->
<section class="skills section" id="skills">
  <h2 class="section__title">Skills</h2>
  <span class="section__subtitle">My Technical Level</span>

  <div class="skills__container container grid">
    <div>
      <!--==================== SKILLS 1 ====================-->
      <div class="skills__content">
        <div class="skills__header">
          <i class="uil uil-brackets-curly skills__icon"></i>

          <div>
            <h1 class="skills__title">Frontend Developer</h1>
            <span class="skills__subtitle">More than 4 years</span>
          </div>

            <i class="uil uil-angle-down skills__arrow"></i>
        </div>

        <div class="skills__list grid">
          <div class="skills__data">
            <div class="skills__title">
              <h3 class="skills__name">HTML</h3>
              <span class="skills__number">90%</span>
            </div>
            <div class="skills__bar">
              <span class="skills__percentage skills__html"></span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
```

Preview.
![](/readme-img/Skills2.png)

4. Now we fill our other frontend and backend skills.
```
<!--==================== SKILLS ====================-->
<section class="skills section" id="skills">
  <h2 class="section__title">Skills</h2>
  <span class="section__subtitle">My Technical Level</span>

  <div class="skills__container container grid">
    <div>
      <!--==================== FRONTEND SKILLS ====================-->
      <div class="skills__content">
        <div class="skills__header">
          <i class="uil uil-brackets-curly skills__icon"></i>

          <div>
            <h1 class="skills__title">Frontend Developer</h1>
            <span class="skills__subtitle">More than 4 years</span>
          </div>

            <i class="uil uil-angle-down skills__arrow"></i>
        </div>

        <div class="skills__list grid">
          <div class="skills__data">
            <div class="skills__title">
              <h3 class="skills__name">HTML, CSS & Bootstrap</h3>
              <span class="skills__number">90%</span>
            </div>
            <div class="skills__bar">
              <span class="skills__percentage skills__htmlcss"></span>
            </div>
          </div>

          <div class="skills__data">
            <div class="skills__title">
              <h3 class="skills__name">JavaScript</h3>
              <span class="skills__number">60%</span>
            </div>
            <div class="skills__bar">
              <span class="skills__percentage skills__js"></span>
            </div>
          </div>

        </div>
      </div>
      <!--==================== BACKEND SKILLS ====================-->
      <div class="skills__content">
        <div class="skills__header">
          <i class="uil uil-server-network skills__icon"></i>

          <div>
            <h1 class="skills__title">Backend Developer</h1>
            <span class="skills__subtitle">More than 2 years</span>
          </div>

            <i class="uil uil-angle-down skills__arrow"></i>
        </div>

        <div class="skills__list grid">
          <div class="skills__data">
            <div class="skills__title">
              <h3 class="skills__name">Ruby & Rails</h3>
              <span class="skills__number">90%</span>
            </div>
            <div class="skills__bar">
              <span class="skills__percentage skills__ror"></span>
            </div>
          </div>

          <div class="skills__data">
            <div class="skills__title">
              <h3 class="skills__name">Python & Django</h3>
              <span class="skills__number">30%</span>
            </div>
            <div class="skills__bar">
              <span class="skills__percentage skills__python"></span>
            </div>
          </div>

          <div class="skills__data">
            <div class="skills__title">
              <h3 class="skills__name">PHP & Laravel</h3>
              <span class="skills__number">10%</span>
            </div>
            <div class="skills__bar">
              <span class="skills__percentage skills__php"></span>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div>
</section>
```

Preview.
![](/readme-img/Skills3.png)

5. We add another div for our data and reports skills.
```
<div>
  <!--==================== DATA & REPORTS SKILLS ====================-->
  <div class="skills__content">
    <div class="skills__header">
      <i class="uil uil-brain skills__icon"></i>

      <div>
        <h1 class="skills__title">Data & Reports Engineer</h1>
        <span class="skills__subtitle">More than 4 years</span>
      </div>

        <i class="uil uil-angle-down skills__arrow"></i>
    </div>

    <div class="skills__list grid">
      <div class="skills__data">
        <div class="skills__title">
          <h3 class="skills__name">Excel VBA & Googlesheets</h3>
          <span class="skills__number">95%</span>
        </div>
        <div class="skills__bar">
          <span class="skills__percentage skills__ror"></span>
        </div>
      </div>

      <div class="skills__data">
        <div class="skills__title">
          <h3 class="skills__name">UiPath & Web Scraping</h3>
          <span class="skills__number">70%</span>
        </div>
        <div class="skills__bar">
          <span class="skills__percentage skills__python"></span>
        </div>
      </div>

      <div class="skills__data">
        <div class="skills__title">
          <h3 class="skills__name">SQL</h3>
          <span class="skills__number">10%</span>
        </div>
        <div class="skills__bar">
          <span class="skills__percentage skills__php"></span>
        </div>
      </div>

    </div>
  </div>
</div>
```

Preview.
![](/readme-img/Skills4.png)

### assets/css/styles.css
1. Now it's time to add some styling for our 'skills' section.
```
/*==================== SKILLS ====================*/
.skills__container{
  row-gap: 0;
}

.skills__header{
  display: flex;
  align-items: center;
  margin-bottom: var(--mb-2-5);
  cursor: pointer;
}

.skills__icon,
.skills__arrow{
  font-size: 2rem;
  color: var(--first-color);
}

.skills__icon{
  margin-right: var(--mb-0-75);
}
```

Preview.
![](/readme-img/Skills5.png)

2. Then we adjust the size of the skill title and subtitle.
```
/*==================== SKILLS ====================*/
.skills__container{
  row-gap: 0;
}

.skills__header{
  display: flex;
  align-items: center;
  margin-bottom: var(--mb-2-5);
  cursor: pointer;
}

.skills__icon,
.skills__arrow{
  font-size: 2rem;
  color: var(--first-color);
}

.skills__icon{
  margin-right: var(--mb-0-75);
}

.skills__title{
  font-size: var(--h3-font-size);
}

.skills__subtitle{
  font-size: var(--small-font-size);
  color: var(--text-color-light);
}
```

3. We'll have the skill and progress percentage in a single line.
Note that we change the '.skills__title' to '.skills__titles'.
```
/*==================== SKILLS ====================*/
.skills__container{
  row-gap: 0;
}

.skills__header{
  display: flex;
  align-items: center;
  margin-bottom: var(--mb-2-5);
  cursor: pointer;
}

.skills__icon,
.skills__arrow{
  font-size: 2rem;
  color: var(--first-color);
}

.skills__icon{
  margin-right: var(--mb-0-75);
}

.skills__titles{
  font-size: var(--h3-font-size);
}

.skills__subtitle{
  font-size: var(--small-font-size);
  color: var(--text-color-light);
}

.skills__arrow{
  margin-left: auto;
  transition: 0.4s;
}

.skills__titles{
  display: flex;
  justify-content: space-between;
  margin-bottom: var(--mb-0-5);
}
```

Preview.
![](/readme-img/Skills6.png)

4. Fix the font-size and font-weight of the skill names.
```
/*==================== SKILLS ====================*/
.skills__container{
  row-gap: 0;
}

.skills__header{
  display: flex;
  align-items: center;
  margin-bottom: var(--mb-2-5);
  cursor: pointer;
}

.skills__icon,
.skills__arrow{
  font-size: 2rem;
  color: var(--first-color);
}

.skills__icon{
  margin-right: var(--mb-0-75);
}

.skills__titles{
  font-size: var(--h3-font-size);
}

.skills__subtitle{
  font-size: var(--small-font-size);
  color: var(--text-color-light);
}

.skills__arrow{
  margin-left: auto;
  transition: 0.4s;
}

.skills__titles{
  display: flex;
  justify-content: space-between;
  margin-bottom: var(--mb-0-5);
}

.skills__name{
  font-size: var(--normal-font-size);
  font-weight: var(--font-medium);
}
```

Preview.
![](/readme-img/Skills7.png)

5. Add a progress bar for each skills.
```
/*==================== SKILLS ====================*/
.skills__container{
  row-gap: 0;
}

.skills__header{
  display: flex;
  align-items: center;
  margin-bottom: var(--mb-2-5);
  cursor: pointer;
}

.skills__icon,
.skills__arrow{
  font-size: 2rem;
  color: var(--first-color);
}

.skills__icon{
  margin-right: var(--mb-0-75);
}

.skills__titles{
  font-size: var(--h3-font-size);
}

.skills__subtitle{
  font-size: var(--small-font-size);
  color: var(--text-color-light);
}

.skills__arrow{
  margin-left: auto;
  transition: 0.4s;
}

.skills__titles{
  display: flex;
  justify-content: space-between;
  margin-bottom: var(--mb-0-5);
}

.skills__name{
  font-size: var(--normal-font-size);
  font-weight: var(--font-medium);
}

.skills__bar,
.skills__percentage{
  height: 5px;
  border-radius: 0.25rem;
}

.skills__bar{
  background-color: var(--first-color-lighter);
}
```

Preview.
![](/readme-img/Skills8.png)

6. Add status for each progress bar.
```
/*==================== SKILLS ====================*/
.skills__container{
  row-gap: 0;
}

.skills__header{
  display: flex;
  align-items: center;
  margin-bottom: var(--mb-2-5);
  cursor: pointer;
}

.skills__icon,
.skills__arrow{
  font-size: 2rem;
  color: var(--first-color);
}

.skills__icon{
  margin-right: var(--mb-0-75);
}

.skills__titles{
  font-size: var(--h3-font-size);
}

.skills__subtitle{
  font-size: var(--small-font-size);
  color: var(--text-color-light);
}

.skills__arrow{
  margin-left: auto;
  transition: 0.4s;
}

.skills__titles{
  display: flex;
  justify-content: space-between;
  margin-bottom: var(--mb-0-5);
}

.skills__name{
  font-size: var(--normal-font-size);
  font-weight: var(--font-medium);
}

.skills__bar,
.skills__percentage{
  height: 5px;
  border-radius: 0.25rem;
}

.skills__bar{
  background-color: var(--first-color-lighter);
}

.skills__percentage{
  display: block;
  background-color: var(--first-color);
}

.skills__htmlcss{
  width: 80%;
}

.skills__js{
  width: 60%;
}

.skills__ror{
  width: 90%;
}

.skills__python{
  width: 60%;
}

.skills__php{
  width: 20%;
}

.skills__excel{
  width: 95%;
}

.skills__uipath{
  width: 70%;
}

.skills__sql{
  width: 20%;
}
```

Preview.
![](/readme-img/Skills9.png)

7. Add a left padding for each skills.
```
/*==================== SKILLS ====================*/
.skills__container{
  row-gap: 0;
}

.skills__header{
  display: flex;
  align-items: center;
  margin-bottom: var(--mb-2-5);
  cursor: pointer;
}

.skills__icon,
.skills__arrow{
  font-size: 2rem;
  color: var(--first-color);
}

.skills__icon{
  margin-right: var(--mb-0-75);
}

.skills__titles{
  font-size: var(--h3-font-size);
}

.skills__subtitle{
  font-size: var(--small-font-size);
  color: var(--text-color-light);
}

.skills__arrow{
  margin-left: auto;
  transition: 0.4s;
}

.skills__list{
  row-gap: 1.5rem;
  padding-left: 2.7rem;
}

.skills__titles{
  display: flex;
  justify-content: space-between;
  margin-bottom: var(--mb-0-5);
}

.skills__name{
  font-size: var(--normal-font-size);
  font-weight: var(--font-medium);
}

.skills__bar,
.skills__percentage{
  height: 5px;
  border-radius: 0.25rem;
}

.skills__bar{
  background-color: var(--first-color-lighter);
}

.skills__percentage{
  display: block;
  background-color: var(--first-color);
}

.skills__htmlcss{
  width: 80%;
}

.skills__js{
  width: 60%;
}

.skills__ror{
  width: 90%;
}

.skills__python{
  width: 60%;
}

.skills__php{
  width: 20%;
}

.skills__excel{
  width: 95%;
}

.skills__uipath{
  width: 70%;
}

.skills__sql{
  width: 20%;
}
```

Preview.
![](/readme-img/Skills10.png)

### index.html
6. Now let's add a class 'skills__open'for our first set of skills and 'skills__close' for the rest.
```
<!--==================== SKILLS ====================-->
<section class="skills section" id="skills">
  <h2 class="section__title">Skills</h2>
  <span class="section__subtitle">My Technical Level</span>

  <div class="skills__container container grid">
    <div>
      <!--==================== FRONTEND SKILLS ====================-->
      <div class="skills__content skills__open">
        <div class="skills__header">
          <i class="uil uil-brackets-curly skills__icon"></i>

          <div>
            <h1 class="skills__titles">Frontend Developer</h1>
            <span class="skills__subtitle">More than 4 years</span>
          </div>

            <i class="uil uil-angle-down skills__arrow"></i>
        </div>

        <div class="skills__list grid">
          <div class="skills__data">
            <div class="skills__titles">
              <h3 class="skills__name">HTML, CSS & Bootstrap</h3>
              <span class="skills__number">80%</span>
            </div>
            <div class="skills__bar">
              <span class="skills__percentage skills__htmlcss"></span>
            </div>
          </div>

          <div class="skills__data">
            <div class="skills__titles">
              <h3 class="skills__name">JavaScript</h3>
              <span class="skills__number">60%</span>
            </div>
            <div class="skills__bar">
              <span class="skills__percentage skills__js"></span>
            </div>
          </div>

        </div>
      </div>
      <!--==================== BACKEND SKILLS ====================-->
      <div class="skills__content skills__close">
        <div class="skills__header">
          <i class="uil uil-server-network skills__icon"></i>

          <div>
            <h1 class="skills__titles">Backend Developer</h1>
            <span class="skills__subtitle">More than 2 years</span>
          </div>

            <i class="uil uil-angle-down skills__arrow"></i>
        </div>

        <div class="skills__list grid">
          <div class="skills__data">
            <div class="skills__titles">
              <h3 class="skills__name">Ruby & Rails</h3>
              <span class="skills__number">90%</span>
            </div>
            <div class="skills__bar">
              <span class="skills__percentage skills__ror"></span>
            </div>
          </div>

          <div class="skills__data">
            <div class="skills__titles">
              <h3 class="skills__name">Python & Django</h3>
              <span class="skills__number">60%</span>
            </div>
            <div class="skills__bar">
              <span class="skills__percentage skills__python"></span>
            </div>
          </div>

          <div class="skills__data">
            <div class="skills__titles">
              <h3 class="skills__name">PHP & Laravel</h3>
              <span class="skills__number">20%</span>
            </div>
            <div class="skills__bar">
              <span class="skills__percentage skills__php"></span>
            </div>
          </div>

        </div>
      </div>
    </div>

    <div>
      <!--==================== DATA & REPORTS SKILLS ====================-->
      <div class="skills__content skills__close">
        <div class="skills__header">
          <i class="uil uil-brain skills__icon"></i>

          <div>
            <h1 class="skills__titles">Data & Reports Engineer</h1>
            <span class="skills__subtitle">More than 4 years</span>
          </div>

            <i class="uil uil-angle-down skills__arrow"></i>
        </div>

        <div class="skills__list grid">
          <div class="skills__data">
            <div class="skills__titles">
              <h3 class="skills__name">Excel VBA & Googlesheets</h3>
              <span class="skills__number">95%</span>
            </div>
            <div class="skills__bar">
              <span class="skills__percentage skills__excel"></span>
            </div>
          </div>

          <div class="skills__data">
            <div class="skills__titles">
              <h3 class="skills__name">UiPath & Web Scraping</h3>
              <span class="skills__number">70%</span>
            </div>
            <div class="skills__bar">
              <span class="skills__percentage skills__uipath"></span>
            </div>
          </div>

          <div class="skills__data">
            <div class="skills__titles">
              <h3 class="skills__name">SQL</h3>
              <span class="skills__number">20%</span>
            </div>
            <div class="skills__bar">
              <span class="skills__percentage skills__sql"></span>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div>
</section>
```

### assets/css/styles.css
8. Next we'll create some styling for the list under 'skills__close'.
This will hide skills listed under this subsection.
Please note that we add a margin bottom for 'skills__open'.
```
/*==================== SKILLS ====================*/
.skills__container{
  row-gap: 0;
}

.skills__header{
  display: flex;
  align-items: center;
  margin-bottom: var(--mb-2-5);
  cursor: pointer;
}

.skills__icon,
.skills__arrow{
  font-size: 2rem;
  color: var(--first-color);
}

.skills__icon{
  margin-right: var(--mb-0-75);
}

.skills__titles{
  font-size: var(--h3-font-size);
}

.skills__subtitle{
  font-size: var(--small-font-size);
  color: var(--text-color-light);
}

.skills__arrow{
  margin-left: auto;
  transition: 0.4s;
}

.skills__list{
  row-gap: 1.5rem;
  padding-left: 2.7rem;
}

.skills__titles{
  display: flex;
  justify-content: space-between;
  margin-bottom: var(--mb-0-5);
}

.skills__name{
  font-size: var(--normal-font-size);
  font-weight: var(--font-medium);
}

.skills__bar,
.skills__percentage{
  height: 5px;
  border-radius: 0.25rem;
}

.skills__bar{
  background-color: var(--first-color-lighter);
}

.skills__percentage{
  display: block;
  background-color: var(--first-color);
}

.skills__htmlcss{
  width: 80%;
}

.skills__js{
  width: 60%;
}

.skills__ror{
  width: 90%;
}

.skills__python{
  width: 60%;
}

.skills__php{
  width: 20%;
}

.skills__excel{
  width: 95%;
}

.skills__uipath{
  width: 70%;
}

.skills__sql{
  width: 20%;
}

.skills__close .skills__list{
  height: 0;
  overflow: hidden;
}

.skills__open  .skills__list{
  height: max-content;
  margin-bottom: var(--mb-2-5);
}
```

Preview.
![](/readme-img/Skills11.png)

9. Now we're going to rotate the 'skills__arrow' when the skillset of the subsection is open.
```
/*==================== SKILLS ====================*/
.skills__container{
  row-gap: 0;
}

.skills__header{
  display: flex;
  align-items: center;
  margin-bottom: var(--mb-2-5);
  cursor: pointer;
}

.skills__icon,
.skills__arrow{
  font-size: 2rem;
  color: var(--first-color);
}

.skills__icon{
  margin-right: var(--mb-0-75);
}

.skills__titles{
  font-size: var(--h3-font-size);
}

.skills__subtitle{
  font-size: var(--small-font-size);
  color: var(--text-color-light);
}

.skills__arrow{
  margin-left: auto;
  transition: 0.4s;
}

.skills__list{
  row-gap: 1.5rem;
  padding-left: 2.7rem;
}

.skills__titles{
  display: flex;
  justify-content: space-between;
  margin-bottom: var(--mb-0-5);
}

.skills__name{
  font-size: var(--normal-font-size);
  font-weight: var(--font-medium);
}

.skills__bar,
.skills__percentage{
  height: 5px;
  border-radius: 0.25rem;
}

.skills__bar{
  background-color: var(--first-color-lighter);
}

.skills__percentage{
  display: block;
  background-color: var(--first-color);
}

.skills__htmlcss{
  width: 80%;
}

.skills__js{
  width: 60%;
}

.skills__ror{
  width: 90%;
}

.skills__python{
  width: 60%;
}

.skills__php{
  width: 20%;
}

.skills__excel{
  width: 95%;
}

.skills__uipath{
  width: 70%;
}

.skills__sql{
  width: 20%;
}

.skills__close .skills__list{
  height: 0;
  overflow: hidden;
}

.skills__open  .skills__list{
  height: max-content;
  margin-bottom: var(--mb-2-5);
}

.skills__open .skills__arrow{
  transform: rotate(-180deg);
}
```

Preview.
![](/readme-img/Skills12.png)

### /assets/js/main.js
1. Now let's create an accordion in js to facilitate our open and close effect for our skills.
```
/*==================== ACCORDION SKILLS ====================*/
const skillsContent = document.getElementsByClassName('skills__content'),
      skillsHeader = document.querySelectorAll('.skills__header')

function toggleSkills(){
  let itemClass = this.parentNode.className

  for(i = 0; i < skillsContent.length; i++){
    skillsContent[i].className = 'skills__content skills__close'
  }
  if (itemClass === 'skills__content skills__close') {
    this.parentNode.className = 'skills__content skills__open'
  }
}

skillsHeader.forEach((el) => {
  el.addEventListener('click', toggleSkills)
})
```

Preview.
![](/readme-img/Skills13.png)

## J. Qualification
### index.html
1. Now we will create a qualification section for our work experience.
```
<!--==================== QUALIFICATION ====================-->
<section class="qualification section">
  <h2 class="section__title">Qualification</h2>
  <span class="section__subtitle">My Personal Journey</span>
</section>
```

Preview.
![](/readme-img/Qualification1.png)

2. Let's add an education and work subsection.
```
<!--==================== QUALIFICATION ====================-->
<section class="qualification section">
  <h2 class="section__title">Qualification</h2>
  <span class="section__subtitle">My Personal Journey</span>

  <div class="qualification__container container">
    <div class="qualification__tabs">
      <div class="qualification__button button--flex">
        <i class="uil uil-graduation-cap qualification__icon"></i>
        Education
      </div>

      <div class="qualification__button button--flex">
        <i class="uil uil-briefcase-alt qualification__icon"></i>
        Work
      </div>
    </div>
  </div>
</section>
```

Preview.
![](/readme-img/Qualification2.png)

3. Next let's add the rest of our experience.
```
<!--==================== QUALIFICATION ====================-->
<section class="qualification section">
  <h2 class="section__title">Qualification</h2>
  <span class="section__subtitle">My Personal Journey</span>

  <div class="qualification__container container">
    <div class="qualification__tabs">
      <div class="qualification__button button--flex">
        <i class="uil uil-graduation-cap qualification__icon"></i>
        Education
      </div>

      <div class="qualification__button button--flex">
        <i class="uil uil-briefcase-alt qualification__icon"></i>
        Work
      </div>
    </div>

    <div class="qualification__sections">
      <!--==================== QUALIFICATION CONTENT ====================-->
      <div class="qualification__content">
        <!--==================== EDUCATION QUALIFICATION 1 ====================-->
        <div class="qualification__data">
          <div>
            <h3 class="qualification__title">BS Materials Science & Engineering</h3>
            <span class="qualification__subtitle">University of the Philippines Diliman</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2008 - 2013
            </div>
          </div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 1 ====================-->
        <div class="qualification__data">
          <div></div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>

          <div>
            <h3 class="qualification__title">Operations Executive</h3>
            <span class="qualification__subtitle">Cropital - Crowdfunding Startup</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2013 - 2014
            </div>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 2 ====================-->
        <div class="qualification__data">
          <div></div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>

          <div>
            <h3 class="qualification__title">Data and Reports Analyst</h3>
            <span class="qualification__subtitle">Alorica - Bank Clients</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2014 - 2019
            </div>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 3 ====================-->
        <div class="qualification__data">
          <div></div>

          <div>
            <span class="qualification__rounder"></span>
            <!-- <span class="qualification__line"></span> -->
          </div>

          <div>
            <h3 class="qualification__title">Business and Technical Operations Analyst</h3>
            <span class="qualification__subtitle">Insoon - Beauty eCommerce Startup</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2019 - Current
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>
</section>
```

Preview.
![](/readme-img/Qualification3.png)

4. Create another div for other experiences.
```
<!--==================== QUALIFICATION ====================-->
<section class="qualification section">
  <h2 class="section__title">Qualification</h2>
  <span class="section__subtitle">My Personal Journey</span>

  <div class="qualification__container container">
    <div class="qualification__tabs">
      <div class="qualification__button button--flex">
        <i class="uil uil-graduation-cap qualification__icon"></i>
        Education
      </div>

      <div class="qualification__button button--flex">
        <i class="uil uil-briefcase-alt qualification__icon"></i>
        Work
      </div>
    </div>

    <div class="qualification__sections">
      <!--==================== QUALIFICATION CONTENT 1 ====================-->
      <div class="qualification__content">
        <!--==================== EDUCATION QUALIFICATION 1 ====================-->
        <div class="qualification__data">
          <div>
            <h3 class="qualification__title">BS Materials Science & Engineering</h3>
            <span class="qualification__subtitle">University of the Philippines Diliman</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2008 - 2013
            </div>
          </div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 1 ====================-->
        <div class="qualification__data">
          <div></div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>

          <div>
            <h3 class="qualification__title">Operations Executive</h3>
            <span class="qualification__subtitle">Cropital - Crowdfunding Startup</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2013 - 2014
            </div>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 2 ====================-->
        <div class="qualification__data">
          <div></div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>

          <div>
            <h3 class="qualification__title">Data and Reports Analyst</h3>
            <span class="qualification__subtitle">Alorica - Bank Clients</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2014 - 2019
            </div>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 3 ====================-->
        <div class="qualification__data">
          <div></div>

          <div>
            <span class="qualification__rounder"></span>
            <!-- <span class="qualification__line"></span> -->
          </div>

          <div>
            <h3 class="qualification__title">Business and Technical Operations Analyst</h3>
            <span class="qualification__subtitle">Insoon - Beauty eCommerce Startup</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2019 - Current
            </div>
          </div>
        </div>

      </div>

      <!--==================== QUALIFICATION CONTENT 2 ====================-->
      <div class="qualification__content">
        <!--==================== EDUCATION QUALIFICATION 1 ====================-->
        <div class="qualification__data">
          <div>
            <h3 class="qualification__title">Software Engineer</h3>
            <span class="qualification__subtitle">Microsoft</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2016 - 2018
            </div>
          </div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 1 ====================-->
        <div class="qualification__data">
          <div></div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>

          <div>
            <h3 class="qualification__title">Frontend Developer</h3>
            <span class="qualification__subtitle">Apple Inc</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2018 - 2020
            </div>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 2 ====================-->
        <div class="qualification__data">
          <div>
            <h3 class="qualification__title">Ui Designer</h3>
            <span class="qualification__subtitle">Figma</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2017 - 2018
            </div>
          </div>

          <div>
            <span class="qualification__rounder"></span>
            <!-- <span class="qualification__line"></span> -->
          </div>
        </div>

      </div>
    </div>
  </div>
</section>
```

### /assets/css/styles.css
1. Now we're going to add styling and alignment for our education and work tabs.
```
/*==================== QUALIFICATION ====================*/
.qualification__tabs{
  display: flex;
  justify-content: space-evenly;
  margin-bottom: var(--mb-2);
}

.qualification__button{
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
  cursor: pointer;
}
```

Preview.
![](/readme-img/Qualification4.png)

2. Next we add a hover effect for the two tabs and increase their size.
```
/*==================== QUALIFICATION ====================*/
.qualification__tabs{
  display: flex;
  justify-content: space-evenly;
  margin-bottom: var(--mb-2);
}

.qualification__button{
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
  cursor: pointer;
}

.qualification__button:hover{
  color: var(--first-color);
}

.qualification__icon{
  font-size: 1.8rem;
  margin-right: var(--mb-0-25);
}
```

3. Now we'll be dividing the work and education experience. (Need to fix later.)
```
/*==================== QUALIFICATION ====================*/
.qualification__tabs{
  display: flex;
  justify-content: space-evenly;
  margin-bottom: var(--mb-2);
}

.qualification__button{
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
  cursor: pointer;
}

.qualification__button:hover{
  color: var(--first-color);
}

.qualification__icon{
  font-size: 1.8rem;
  margin-right: var(--mb-0-25);
}

.qualification__data{
  display: grid;
  grid-template-columns: 1fr max-content 1fr;
  column-gap: 1.5rem;
}
```

Preview.
![](/readme-img/Qualification5.png)


4. Adjust the font-size and styling of the qualification name, subtitle and time period.
```
/*==================== QUALIFICATION ====================*/
.qualification__tabs{
  display: flex;
  justify-content: space-evenly;
  margin-bottom: var(--mb-2);
}

.qualification__button{
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
  cursor: pointer;
}

.qualification__button:hover{
  color: var(--first-color);
}

.qualification__icon{
  font-size: 1.8rem;
  margin-right: var(--mb-0-25);
}

.qualification__data{
  display: grid;
  grid-template-columns: 1fr max-content 1fr;
  column-gap: 1.5rem;
}

.qualification__title{
  font-size: var(--normal-font-size);
  font-weight: var(--font-medium);
}

.qualification__subtitle{
  display: inline-block;
  font-size: var(--small-font-size);
  margin-bottom: var(--mb-1);
}

.qualification__calendar{
  font-size: var(--smaller-font-size);
  color: var(--text-color-light);
}
```
Preview.
![](/readme-img/Qualification6.png)


### index.html
1. Now we add a bullet point per qualification line and we double the code block for div Qualification Content.
```
<!--==================== QUALIFICATION ====================-->
<section class="qualification section">
  <h2 class="section__title">Qualification</h2>
  <span class="section__subtitle">My Personal Journey</span>

  <div class="qualification__container container">
    <div class="qualification__tabs">
      <div class="qualification__button button--flex">
        <i class="uil uil-graduation-cap qualification__icon"></i>
        Education
      </div>

      <div class="qualification__button button--flex">
        <i class="uil uil-briefcase-alt qualification__icon"></i>
        Work
      </div>
    </div>

    <div class="qualification__sections">
      <!--==================== QUALIFICATION CONTENT 1 ====================-->
      <div class="qualification__content qualification__active" data-content id="education">
        <!--==================== EDUCATION QUALIFICATION 1 ====================-->
        <div class="qualification__data">
          <div>
            <h3 class="qualification__title">BS Materials Science & Engineering</h3>
            <span class="qualification__subtitle">University of the Philippines Diliman</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2008 - 2013
            </div>
          </div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 1 ====================-->
        <div class="qualification__data">
          <div></div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>

          <div>
            <h3 class="qualification__title">Operations Executive</h3>
            <span class="qualification__subtitle">Cropital - Crowdfunding Startup</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2013 - 2014
            </div>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 2 ====================-->
        <div class="qualification__data">
          <div></div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>

          <div>
            <h3 class="qualification__title">Data and Reports Analyst</h3>
            <span class="qualification__subtitle">Alorica - Bank Clients</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2014 - 2019
            </div>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 3 ====================-->
        <div class="qualification__data">
          <div></div>

          <div>
            <span class="qualification__rounder"></span>
            <!-- <span class="qualification__line"></span> -->
          </div>

          <div>
            <h3 class="qualification__title">Business and Technical Operations Analyst</h3>
            <span class="qualification__subtitle">Insoon - Beauty eCommerce Startup</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2019 - Current
            </div>
          </div>
        </div>

      </div>

      <!--==================== QUALIFICATION CONTENT 2 ====================-->
      <div class="qualification__content"  data-content id="work">
        <!--==================== EDUCATION QUALIFICATION 1 ====================-->
        <div class="qualification__data">
          <div>
            <h3 class="qualification__title">Software Engineer</h3>
            <span class="qualification__subtitle">Microsoft</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2016 - 2018
            </div>
          </div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 1 ====================-->
        <div class="qualification__data">
          <div></div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>

          <div>
            <h3 class="qualification__title">Frontend Developer</h3>
            <span class="qualification__subtitle">Apple Inc</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2018 - 2020
            </div>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 2 ====================-->
        <div class="qualification__data">
          <div>
            <h3 class="qualification__title">Ui Designer</h3>
            <span class="qualification__subtitle">Figma</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2017 - 2018
            </div>
          </div>

          <div>
            <span class="qualification__rounder"></span>
            <!-- <span class="qualification__line"></span> -->
          </div>
        </div>

      </div>
    </div>
  </div>
</section>
```

### /assets/css/styles.css
1. Now we're going to hide the contents of the each qualification tab.
```
/*==================== QUALIFICATION ====================*/
.qualification__tabs{
  display: flex;
  justify-content: space-evenly;
  margin-bottom: var(--mb-2);
}

.qualification__button{
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
  cursor: pointer;
}

.qualification__button:hover{
  color: var(--first-color);
}

.qualification__icon{
  font-size: 1.8rem;
  margin-right: var(--mb-0-25);
}

.qualification__data{
  display: grid;
  grid-template-columns: 1fr max-content 1fr;
  column-gap: 1.5rem;
}

.qualification__title{
  font-size: var(--normal-font-size);
  font-weight: var(--font-medium);
}

.qualification__subtitle{
  display: inline-block;
  font-size: var(--small-font-size);
  margin-bottom: var(--mb-1);
}

.qualification__calendar{
  font-size: var(--smaller-font-size);
  color: var(--text-color-light);
}

.qualification__rounder{
  display: inline-block;
  width: 13px;
  height: 13px;
  background-color: var(--first-color);
  border-radius: 50%;
}

.qualification [data-content]{
  display: none;
}
```

Preview.
![](/readme-img/Qualification7.png)

2. Now we're going to show the content of the qualification tab and add a vertical line piercing all the bullets.
```
/*==================== QUALIFICATION ====================*/
.qualification__tabs{
  display: flex;
  justify-content: space-evenly;
  margin-bottom: var(--mb-2);
}

.qualification__button{
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
  cursor: pointer;
}

.qualification__button:hover{
  color: var(--first-color);
}

.qualification__icon{
  font-size: 1.8rem;
  margin-right: var(--mb-0-25);
}

.qualification__data{
  display: grid;
  grid-template-columns: 1fr max-content 1fr;
  column-gap: 1.5rem;
}

.qualification__title{
  font-size: var(--normal-font-size);
  font-weight: var(--font-medium);
}

.qualification__subtitle{
  display: inline-block;
  font-size: var(--small-font-size);
  margin-bottom: var(--mb-1);
}

.qualification__calendar{
  font-size: var(--smaller-font-size);
  color: var(--text-color-light);
}

.qualification__rounder{
  display: inline-block;
  width: 13px;
  height: 13px;
  background-color: var(--first-color);
  border-radius: 50%;
}

.qualification [data-content]{
  display: none;
}

.qualification__active[data-content]{
  display: block;
}

.qualification__line{
  display: block;
  width: 1px;
  height: 100%;
  background-color: var(--first-color);
  transform: translate(6px,-7px);
}
```

Preview.
![](/readme-img/Qualification8.png)


### /assets/js/main.js
1. Let's add a js effect so the tabs show the correct qualification when you click them and hide the other.
```
/*==================== QUALIFICATION TABS ====================*/
const tabs = document.querySelectorAll('[data-target]'),
      tabContents = document.querySelectorAll('[data-content]')

tabs.forEach(tab =>{
  tab.addEventListener('click', ()=>{
      const target = document.querySelector(tab.dataset.tatrget)

      tabContents.forEach(tabContent =>{
        tabContent.classList.remove('qualification__active')
      })
      target.classList.add('qualification__active')

      tabs.forEach(tab =>{
        tab.classList.remove('qualification__active')
      })
      tab.classList.add('qualification__active')
  })
})
```

### index.html
1. Under the 'qualification__tabs' div, update the code with the block below so it will connect with our new js code.
```
<div class="qualification__tabs">
  <div class="qualification__button button--flex qualification__active" data-target='#education'>
    <i class="uil uil-graduation-cap qualification__icon"></i>
    Education
  </div>

  <div class="qualification__button button--flex" data-target='#work'>
    <i class="uil uil-briefcase-alt qualification__icon"></i>
    Work
  </div>
</div>

```

2. Now let's fix the contents of our qualifications.
```
<!--==================== QUALIFICATION ====================-->
<section class="qualification section">
  <h2 class="section__title">Qualification</h2>
  <span class="section__subtitle">My Personal Journey</span>

  <div class="qualification__container container">
    <div class="qualification__tabs">
      <div class="qualification__button button--flex qualification__active" data-target='#education'>
        <i class="uil uil-graduation-cap qualification__icon"></i>
        Education
      </div>

      <div class="qualification__button button--flex" data-target='#work'>
        <i class="uil uil-briefcase-alt qualification__icon"></i>
        Work
      </div>
    </div>

    <div class="qualification__sections">
      <!--==================== QUALIFICATION CONTENT 1 ====================-->
      <div class="qualification__content qualification__active" data-content id="education">
        <!--==================== EDUCATION QUALIFICATION 1 ====================-->
        <div class="qualification__data">
          <div>
            <h3 class="qualification__title">BS Materials Science & Engineering</h3>
            <span class="qualification__subtitle">University of the Philippines Diliman</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2008 - 2013
            </div>
          </div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 1 ====================-->
        <div class="qualification__data">
          <div></div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>

          <div>
            <h3 class="qualification__title">Microsoft Office Suite & Visual Basic Programming</h3>
            <span class="qualification__subtitle">Informatics</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2013 - 2014
            </div>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 2 ====================-->
        <div class="qualification__data">
          <div>
            <h3 class="qualification__title">Web Developer Bootcamp</h3>
            <span class="qualification__subtitle">
              Zuitt - Filipino startup offering web development
              coding bootcamps in Manila, helping shape the future of IT Education in the Philippines.
            </span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2018 - 2019
            </div>
          </div>

          <div>
            <span class="qualification__rounder"></span>
            <!-- <span class="qualification__line"></span> -->
          </div>
        </div>

      </div>

      <!--==================== QUALIFICATION CONTENT 2 ====================-->
      <div class="qualification__content"  data-content id="work">
        <!--==================== EDUCATION QUALIFICATION 1 ====================-->
        <div class="qualification__data">
          <div>
            <h3 class="qualification__title">Operations Executive</h3>
            <span class="qualification__subtitle">Cropital - Philippines 1st Crowdfunding Startup</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2013 - 2014
            </div>
          </div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 1 ====================-->
        <div class="qualification__data">
          <div></div>

          <div>
            <span class="qualification__rounder"></span>
            <span class="qualification__line"></span>
          </div>

          <div>
            <h3 class="qualification__title">Data & Reports Analyst</h3>
            <span class="qualification__subtitle">Alorica - Largest BPO Provider in the Philippines</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2014 - 2019
            </div>
          </div>
        </div>

        <!--==================== WORK QUALIFICATION 2 ====================-->
        <div class="qualification__data">
          <div>
            <h3 class="qualification__title">Business Intelligence Analyst</h3>
            <span class="qualification__subtitle">Insoon - Beauty eCommerce Startup</span>
            <div class="qualification__calendar">
              <i class="uil uil-calendar-alt"></i>
              2019 - 2021
            </div>
          </div>

          <div>
            <span class="qualification__rounder"></span>
            <!-- <span class="qualification__line"></span> -->
          </div>
        </div>

      </div>
    </div>
  </div>
</section>

```

Preview.
![](/readme-img/Qualification9.png)

## K. SERVICES
### index.html
1. Let's create our first service.
```
<!--==================== SERVICES ====================-->
<section class="services section" id="services">
  <h2 class="section__title">Services</h2>
  <span class="section__subtitle">What I offer?</span>

  <div class="services__container container grid">
    <!--==================== SERVICES 1 ====================-->
    <div class="services__content">
      <div>
        <i class="uil uil-web-grid services__icon"></i>
        <h3 class="services__title">UI/UX <br> Designer</h3>
      </div>

      <span class="button button--flex button--small button--link services__button">
        View More
        <i class="uil uil-arrow-right button__icon"></i>
      </span>
    </div>
  </div>

</section>
```

Preview.
![](/readme-img/Services1.png)

2. Next we'll create a modal for our 1st servic (e.g. UI/UX Designer).
```
<div class="services__modal">
  <div class="services__modal-content">
    <h4 class="services__modal-title">UI/UX <br> Designer</h4>
    <i class="uil uil-times services__modal-close"></i>

    <ul class="services__modal-services grid">
      <li class="services__modal-service">
        <i class="uil uil-check-circle services__modal-icon"></i>
        <p>I develop the user interface.</p>
      </li>
      <li class="services__modal-service">
        <i class="uil uil-check-circle services__modal-icon"></i>
        <p>Web page development.</p>
      </li>
      <li class="services__modal-service">
        <i class="uil uil-check-circle services__modal-icon"></i>
        <p>I create UX element interactions.</p>
      </li>
      <li class="services__modal-service">
        <i class="uil uil-check-circle services__modal-icon"></i>
        <p>I position your company brand.</p>
      </li>

    </ul>
  </div>
</div>
```

3. Have 2 more copies of our first service.
```
<div class="services__container container grid">
  <!--==================== SERVICES 1 ====================-->
  <div class="services__content">
    <div>
      <i class="uil uil-web-grid services__icon"></i>
      <h3 class="services__title">UI/UX <br> Designer</h3>
    </div>

    <span class="button button--flex button--small button--link services__button">
      View More
      <i class="uil uil-arrow-right button__icon"></i>
    </span>

    <div class="services__modal">
      <div class="services__modal-content">
        <h4 class="services__modal-title">UI/UX <br> Designer</h4>
        <i class="uil uil-times services__modal-close"></i>

        <ul class="services__modal-services grid">
          <li class="services__modal-service">
            <i class="uil uil-check-circle services__modal-icon"></i>
            <p>I develop the user interface.</p>
          </li>
          <li class="services__modal-service">
            <i class="uil uil-check-circle services__modal-icon"></i>
            <p>Web page development.</p>
          </li>
          <li class="services__modal-service">
            <i class="uil uil-check-circle services__modal-icon"></i>
            <p>I create UX element interactions.</p>
          </li>
          <li class="services__modal-service">
            <i class="uil uil-check-circle services__modal-icon"></i>
            <p>I position your company brand.</p>
          </li>

        </ul>
      </div>
    </div>
  </div>
  <!--==================== SERVICES 2 ====================-->
  <div class="services__content">
    <div>
      <i class="uil uil-web-grid services__icon"></i>
      <h3 class="services__title">UI/UX <br> Designer</h3>
    </div>

    <span class="button button--flex button--small button--link services__button">
      View More
      <i class="uil uil-arrow-right button__icon"></i>
    </span>

    <div class="services__modal">
      <div class="services__modal-content">
        <h4 class="services__modal-title">UI/UX <br> Designer</h4>
        <i class="uil uil-times services__modal-close"></i>

        <ul class="services__modal-services grid">
          <li class="services__modal-service">
            <i class="uil uil-check-circle services__modal-icon"></i>
            <p>I develop the user interface.</p>
          </li>
          <li class="services__modal-service">
            <i class="uil uil-check-circle services__modal-icon"></i>
            <p>Web page development.</p>
          </li>
          <li class="services__modal-service">
            <i class="uil uil-check-circle services__modal-icon"></i>
            <p>I create UX element interactions.</p>
          </li>
          <li class="services__modal-service">
            <i class="uil uil-check-circle services__modal-icon"></i>
            <p>I position your company brand.</p>
          </li>

        </ul>
      </div>
    </div>
  </div>
  <!--==================== SERVICES 3 ====================-->
  <div class="services__content">
    <div>
      <i class="uil uil-web-grid services__icon"></i>
      <h3 class="services__title">UI/UX <br> Designer</h3>
    </div>

    <span class="button button--flex button--small button--link services__button">
      View More
      <i class="uil uil-arrow-right button__icon"></i>
    </span>

    <div class="services__modal">
      <div class="services__modal-content">
        <h4 class="services__modal-title">UI/UX <br> Designer</h4>
        <i class="uil uil-times services__modal-close"></i>

        <ul class="services__modal-services grid">
          <li class="services__modal-service">
            <i class="uil uil-check-circle services__modal-icon"></i>
            <p>I develop the user interface.</p>
          </li>
          <li class="services__modal-service">
            <i class="uil uil-check-circle services__modal-icon"></i>
            <p>Web page development.</p>
          </li>
          <li class="services__modal-service">
            <i class="uil uil-check-circle services__modal-icon"></i>
            <p>I create UX element interactions.</p>
          </li>
          <li class="services__modal-service">
            <i class="uil uil-check-circle services__modal-icon"></i>
            <p>I position your company brand.</p>
          </li>

        </ul>
      </div>
    </div>
  </div>
</div>
```

Preview.
![](/readme-img/Services2.png)

4. Change the title and modal title for service 2 and 3.

### /assets/css/styles.css
1. We'll create some styling for container and content.
```
/*==================== SERVICES ====================*/
.services__container{
  gap: 1.5rem;
  grid-template-columns: repeat(2, 1fr);
}

.services__content{
  position: relative;
  background-color: var(--container-color);
  padding: 3.5rem 0.5rem 1.25rem;
  border-radius: 0.25rem;
  box-shadow: 0 2px 4px rgba(0,0,0,0.15);
  transition: 0.3s;
}
```
Preview.
![](/readme-img/Services3.png)

2. We'all add a shadow in our content when we hover it and adjust the size and color of our icons.
```
.services__content:hover{
  box-shadow: 0 4px 8px rgba(0,0,0,0.15);
}

.services__icon{
  display: block;
  font-size: 1.5rem;
  color: var(--first-color);
  margin-bottom: var(--mb-1);
}
```

3. We apply styling in our '.services__title' and our '.services__button'.
```
.services__title{
  font-size: var(--h3-font-size);
  margin-bottom: var(--mb-1);
  font-weight: var(--font-medium);
}

.services__button{
  cursor: pointer;
  font-size: var(--small-font-size);
}
```

Preview.
![](/readme-img/Services4.png)

4. Go back to our 'Buttons' section and insert additional styling for our buttons.
```
.button--small{
  padding: 0.75rem 1rem;
}

.button--link{
  padding: 0;
  background-color: transparent;
  color: var(--first-color);
}

.button--link:hover{
  background-color: transparent;
  color: var(--first-color-alt);
}
```

Preview.
![](/readme-img/Services5.png)

5. Go back to the services then we'll add a slide effect when we hover to our '.services__button'.
```
.services__button:hover .button__icon{
  transform: translateX(0.25rem);
}
```

6. Now we're going to style our modal.
```
.services__modal{
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0,0,0,0.5);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 1rem;
  z-index: var(--z-modal);
  /* opacity: 0; */
  /* visibility: hidden; */
  transition: 0.3s;
}
```
Preview.
![](/readme-img/Services7.png)

7. Let's build a box for our modal.
```
.services__modal-content{
  position: relative;
  background-color: var(--container-color);
  padding: 1.5rem;
  border-radius: 0.5rem;
}
```

Preview.
![](/readme-img/Services8.png)

8. Let's fix the row-gap of each description in our modal.
```
.services__modal-services{
  row-gap: 1rem;
}

.services__modal-service{
  display: flex;
}
```

Preview.
![](/readme-img/Services9.png)

9. Add a margin-bottom for our modal service title and add styling.
```
.services__modal-title{
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
  margin-bottom: var(--mb-1-5);
}
```

10. Now we'll be applying color using 'var(--first-color)' and styling for our close and modal icons.
```
.services__modal-close{
  position: absolute;
  top: 1rem;
  right: 1rem;
  font-size: 1.5rem;
  color: var(--first-color);
  cursor: pointer;
}

.services__modal-icon{
  color: var(--first-color);
  margin-right: var(--mb-0-25);
}
```

11. Now let's hide our modal so it will activate only when we click it by uncommenting opacity and visibility.
```
.services__modal{
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0,0,0,0.5);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 1rem;
  z-index: var(--z-modal);
  opacity: 0;
  visibility: hidden;
  transition: 0.3s;
}
```

12. Next let's make sure that when a modal is active it will be visible.
```
/* Active Modal */
.active-modal{
  opacity: 1;
  visibility: visible;
}
```

### /assets/js/main.js
1. Let's a js to control the visibility or show/hide of our modal services.
```
/*==================== SERVICES MODAL ====================*/
const modalViews = document.querySelectorAll('.services__modal'),
      modalBtns = document.querySelectorAll('.services__button'),
      modalCloses = document.querySelectorAll('.services__modal-close')

let modal = function(modalClick){
  modalViews[modalClick].classList.add('active-modal')
}
```

2. Now let's a feature when we click the 'View More' it will show our modal and if we click the 'close' icon' it  will hide our modal.
```
/*==================== SERVICES MODAL ====================*/
const modalViews = document.querySelectorAll('.services__modal'),
      modalBtns = document.querySelectorAll('.services__button'),
      modalCloses = document.querySelectorAll('.services__modal-close')

let modal = function(modalClick){
  modalViews[modalClick].classList.add('active-modal')
}

modalBtns.forEach((modalBtn, i) =>{
  modalBtn.addEventListener('click', ()=>{
    modal(i)
  })
})

modalCloses.forEach((modalClose) =>{
  modalClose.addEventListener('click', ()=>{
    modalViews.forEach((modalView) =>{
      modalView.classList.remove('active-modal')
    })
  })
})
```
## L. PORTFOLIO - PAST PROJECTS
### index.html
1. Let's build our portfolio section.
```
<!--==================== PORTFOLIO ====================-->
<section class="portfolio section" id="portfolio">
  <h2 class="section__title">Portfolio</h2>
  <span class="section__subtitle">Recent Works</span>

  <div class="portfolio__container container">
    <div>
      <!--==================== PORTFOLIO 1 ====================-->
      <div class="portfolio__content grid">
        <img src="assets/img/portfolio1.jpg" alt="" class="portfolio__img">

        <div class="portfolio__data">
          <h3 class="portfolio__title">Modern Website</h3>
          <p class="portfolio__description">
            Website adaptable to all devices, wih UI components and animated interactions.
          </p>
          <a href="#" class="button button--flex button--small portfolio__button">
            Demo
            <i class="uil uil-arrow-right button__icon"></i>
          </a>
        </div>
      </div>

    </div>
  </div>


</section>
```

Preview.
![](/readme-img/Portfolio1.png)

2. Add two more portfolio subsection.
```
<!--==================== PORTFOLIO ====================-->
<section class="portfolio section" id="portfolio">
  <h2 class="section__title">Portfolio</h2>
  <span class="section__subtitle">Recent Works</span>

  <div class="portfolio__container container">
    <div>
      <!--==================== PORTFOLIO 1 ====================-->
      <div class="portfolio__content grid">
        <img src="assets/img/portfolio1.jpg" alt="" class="portfolio__img">

        <div class="portfolio__data">
          <h3 class="portfolio__title">Modern Website</h3>
          <p class="portfolio__description">
            Website adaptable to all devices, wih UI components and animated interactions.
          </p>
          <a href="#" class="button button--flex button--small portfolio__button">
            Demo
            <i class="uil uil-arrow-right button__icon"></i>
          </a>
        </div>
      </div>

      <!--==================== PORTFOLIO 2 ====================-->
      <div class="portfolio__content grid">
        <img src="assets/img/portfolio2.jpg" alt="" class="portfolio__img">

        <div class="portfolio__data">
          <h3 class="portfolio__title">Brand Design</h3>
          <p class="portfolio__description">
            Website adaptable to all devices, wih UI components and animated interactions.
          </p>
          <a href="#" class="button button--flex button--small portfolio__button">
            Demo
            <i class="uil uil-arrow-right button__icon"></i>
          </a>
        </div>
      </div>

      <!--==================== PORTFOLIO 3 ====================-->
      <div class="portfolio__content grid">
        <img src="assets/img/portfolio3.jpg" alt="" class="portfolio__img">

        <div class="portfolio__data">
          <h3 class="portfolio__title">Online Store</h3>
          <p class="portfolio__description">
            Website adaptable to all devices, wih UI components and animated interactions.
          </p>
          <a href="#" class="button button--flex button--small portfolio__button">
            Demo
            <i class="uil uil-arrow-right button__icon"></i>
          </a>
        </div>
      </div>

    </div>
  </div>


</section>
```

### /assets/css/styles.css
1. Let's do an initial overflow for the '.portfolio__container' and padding for the content.
Also let's adjust the size of the portfolio images.
```
/*==================== PORTFOLIO ====================*/
.portfolio__container{
  overflow: initial;
}

.portfolio__content{
  padding: 0 1.5rem;
}

.portfolio__img{
  width: 265px;
  border-radius: 0.5rem;
  justify-self: center;
}
```
Preview.
![](/readme-img/Portfolio2.png)

2. Next let's adjust the font-size and add a margin-bottom for the title and description of our portfolio.
```
.portfolio__title{
  font-size: var(--h3-font-size);
  margin-bottom: var(--mb-0-5);
}

.portfolio__description{
  margin-bottom: var(--mb-0-75);
}
```

3. Add a sliding hover effect in the arrows of our portfolio buttons.
```
.portfolio__button:hover .button__icon{
  transform: translateX(0.25rem);
}
```

### index.html
1. We'll be adding a touch slider framework, 'Swiper JS'.
```
<!--==================== SWIPER CSS ====================-->
<link rel="stylesheet" href="assets/css/swiper-bundle.min.css">
```

```
<!--==================== SWIPER JS ====================-->
<script src="assets/js/swiper-bundle.min.js"></script>
```

2. Next let's add swiper classes in our portfolio section divs. For this we use Swiper JS' CSS mode.
Preview.
![](/readme-img/Portfolio3.png)

3. From the CSS mode in Swiper JS website, we'll copy the code for arrows and pagination.
```
<!-- Swiper JS Arrows -->
<div class="swiper-button-next"></div>
<div class="swiper-button-prev"></div>

<!-- Swiper JS Pagination -->
<div class="swiper-pagination"></div>
```

4. Add custom icons from Iconscout for right and left arrows.
```
<!-- Swiper JS Arrows -->
<div class="swiper-button-next">
  <i class="uil uil-angle-right-b swiper-portfolio-icon"></i>                  
</div>
<div class="swiper-button-prev">
  <i class="uil uil-angle-left-b swiper-portfolio-icon"></i>
</div>
```

### /assets/js/main.js
1. Now let's add a swiper js for the portfolio swiper from the CSS mode.
Take note we replace the target class with ".portfolio__container".
```
/*==================== PORTFOLIO SWIPER  ====================*/
let var swiper = new Swiper(".portfolio__container", {
  cssMode: true,
  navigation: {
    nextEl: ".swiper-button-next",
    prevEl: ".swiper-button-prev",
  },
  pagination: {
    el: ".swiper-pagination",
  },
  mousewheel: true,
  keyboard: true,
});
```

2. Add a loop attribute and disable the mousewheel and keyboard attribute.
```
/*==================== PORTFOLIO SWIPER  ====================*/
let swiper = new Swiper(".portfolio__container", {
  cssMode: true,
  loop: true,

  navigation: {
    nextEl: ".swiper-button-next",
    prevEl: ".swiper-button-prev",
  },
  pagination: {
    el: ".swiper-pagination",
    clickable: true,
  },
  // mousewheel: true,
  // keyboard: true,
});
```

### /assets/css/styles.css
1. Let's remove the arrow templates from swiper so only the Iconscout arrows will show.
```
.swiper-button-prev::after,
.swiper-button-next::after{
  content: '';
}
```

2. We'll increase the size and change the color of our Iconscout arrows.
```
.swiper-portfolio-icon{
  font-size: 2rem;
  color: var(--first-color);
}
```

3. Add a bit of space for our arrows so it is not very close to the content.
```
.swiper-button-prev{
  left: -0.5rem;
}

.swiper-button-next{
  right: -0.5rem;
}
```

4. Let's push down our pagination bullets a bit and change the color of the active bullet.
```
.swiper-container-horizontal > .swiper-pagination-bullets{
  bottom: -2.5rem;
}

.swiper-pagination-bullets-active{
  background-color: var(--first-color);
}
```

5. Let's remove the outline for our swiper arrows and bullets.
```
.swiper-button-prev,
.swiper-button-next,
.swiper-pagination-bullet{
  outline: none;
}
```

Preview.
![](/readme-img/Portfolio4.png)

## K. Project in Mind Jumbotron
### index.html
1. Let's create a 'contact me' banner.
```
<!--==================== PROJECT IN MIND ====================-->
<section class="project section">
  <div class="project__bg">
    <div class="project__container container grid">
      <div class="project__data">
        <h2 class="project__title">You have a new project</h2>
        <p class="project__description">
          Contact me now and get a 30% discount on your new project.
        </p>
        <a href="#contact" class="button button--flex button--white">
          Contact Me
          <i class="uil uil-message project__icon button__icon"></i>
        </a>
      </div>

      <img src="assets/img/project.png" alt="" class="project__img">
    </div>
  </div>

</section>
```
Preview.
![](/readme-img/Project1.png)


### /assets/css/styles.css
1. Add styling for our Jumbotron.
```
/*==================== PROJECT IN MIND ====================*/
.project{
  text-align: center;
}

.project__bg{
  background-color: var(--first-color-second);
  padding-top: 3rem;
}

.project__title{
  font-size: var(--h2-font-size);
  margin-bottom: var(--mb-0-75);
}

.project__description{
  margin-bottom: var(--mb-1-5);
}

.project__title,
.project__description{
  color: #FFF;
}

.project__img{
  width: 232px;
  justify-self: center;
}
```

Preview.
![](/readme-img/Project2.png)

2. Add additional styling for our buttons section.
```
.button--white{
  background-color: #FFF;
  color: var(--first-color);
}

.button--white:hover{
  background-color: #FFF;
}
```
Preview.
![](/readme-img/Project3.png)


## L. TESTIMONIAL
### index.html
1. Create a new section and insert the ff code block. Get the star icons from Iconscout.
```
<!--==================== TESTIMONIAL ====================-->
<section class="testimonial section">
  <h2 class="section__title">Testimonial</h2>
  <span class="section__subtitle">What my Clients are Saying</span>

  <div class="testimonial__container container">
    <div>
      <!--==================== TESTIMONIAL 1 ====================-->
      <div class="testimonial__content">
        <div class="testimonial__data">
          <div class="testimonial__header">
            <img src="assets/img/testimonial1.jpg" alt="" class="testimonial__img">

            <div>
              <h3 class="testimonial__name">Sara Smith</h3>
              <span class="testimonial_client">Client</span>
            </div>
          </div>

          <div>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
          </div>
        </div>

        <p class="testimonial__description">
          I get a good impression,
          I carry out my project with all the possible quality
          and attention and support 24 hours a day.
        </p>
      </div>
    </div>
  </div>

</section>
```

Preview.
![](/readme-img/Testimonial1.png)

2. Create 2 more testimonial divs.
```
<!--==================== TESTIMONIAL ====================-->
<section class="testimonial section">
  <h2 class="section__title">Testimonial</h2>
  <span class="section__subtitle">What my Clients are Saying</span>

  <div class="testimonial__container container">
    <div>
      <!--==================== TESTIMONIAL 1 ====================-->
      <div class="testimonial__content">
        <div class="testimonial__data">
          <div class="testimonial__header">
            <img src="assets/img/testimonial1.jpg" alt="" class="testimonial__img">

            <div>
              <h3 class="testimonial__name">Sara Smith</h3>
              <span class="testimonial_client">Client</span>
            </div>
          </div>

          <div>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
          </div>
        </div>

        <p class="testimonial__description">
          I get a good impression,
          I carry out my project with all the possible quality
          and attention and support 24 hours a day.
        </p>
      </div>

      <!--==================== TESTIMONIAL 2 ====================-->
      <div class="testimonial__content">
        <div class="testimonial__data">
          <div class="testimonial__header">
            <img src="assets/img/testimonial2.jpg" alt="" class="testimonial__img">

            <div>
              <h3 class="testimonial__name">Matt Robinson</h3>
              <span class="testimonial_client">Client</span>
            </div>
          </div>

          <div>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
          </div>
        </div>

        <p class="testimonial__description">
          I get a good impression,
          I carry out my project with all the possible quality
          and attention and support 24 hours a day.
        </p>
      </div>

      <!--==================== TESTIMONIAL 3 ====================-->
      <div class="testimonial__content">
        <div class="testimonial__data">
          <div class="testimonial__header">
            <img src="assets/img/testimonial3.jpg" alt="" class="testimonial__img">

            <div>
              <h3 class="testimonial__name">Raul Harris</h3>
              <span class="testimonial_client">Client</span>
            </div>
          </div>

          <div>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
            <i class="uil uil-star testimonial__icon-star"></i>
          </div>
        </div>

        <p class="testimonial__description">
          I get a good impression,
          I carry out my project with all the possible quality
          and attention and support 24 hours a day.
        </p>
      </div>


    </div>
  </div>

</section>
```

Preview.
![](/readme-img/Testimonial2.png)

### /assets/css/styles.css
1. Now let's create some styling for our testimonials.
```
/*==================== TESTIMONIAL ====================*/
.testimonial__data,
.testimonial__header{
  display: flex;
}

.testimonial__data{
  justify-content: space-between;
  margin-bottom: var(--mb-1-5);
}

.testimonial__img{
  width: 60px;
  height: 60px;
  border-radius: 50%;
  margin-right: var(--mb-0-75);
}
```

Preview.
![](/readme-img/Testimonial3.png)

2. Let's fix the styling of our testimonial name, client and stars.
```
.testimonial__name{
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);.testimonial__name{
    font-size: var(--h3-font-size);
    font-weight: var(--font-medium);
  }

  .testimonial__client{
    font-size: var(--small-font-size);
    color: var(--text-color-light);  
  }

  .testimonial__description{
    margin-bottom: var(--mb-2-5);
  }

  .testimonial__icon-start{
    color: var(--first-color);
  }
```



### index.html
1. Now let's add Swiper JS class using 'pagination dynamic' demo.

Preview.
![](/readme-img/Testimonial5.png)

Preview.
![](/readme-img/Testimonial6.png)

### /assets/js/main.js
1. We'll change the 'swiper' to 'swiperPortfolio' in the Portfolio section.
After that we will add a js for the slider effect of the testimonial.

Preview.
![](/readme-img/Testimonial7.png)

### /assets/css/styles.css
1. Next we'll create styling for our navigation bullets.
```
.swiper-container .swiper-pagination-testimonial{
  bottom: 0;
}
```

Preview.
![](/readme-img/Testimonial8.png)

## M. Contact
### index.html
1. Now let's create a 'contact me' section.
```
<!--==================== CONTACT ME ====================-->
<section class="contact section" id="contact">
  <h2 class="section__title">Contact Me</h2>
  <span class="section__subtitle">Get in Touch</span>

  <div class="contact__container container grid">
    <div>
      <div class="contact__information">
        <i class="uil uil-envelope contact__icon"></i>

        <div>
          <h3 class="contact__title">Email Me</h3>
          <span class="contact__subtitle">johnsteven.tapican@gmail.com</span>
        </div>
      </div>
    </div>
  </div>
</section>
```

Preview.
![](/readme-img/Contact1.png)

2. Add a form to enter name.
```
<!--==================== CONTACT ME ====================-->
<section class="contact section" id="contact">
  <h2 class="section__title">Contact Me</h2>
  <span class="section__subtitle">Get in Touch</span>

  <div class="contact__container container grid">
    <div>
      <div class="contact__information">
        <i class="uil uil-envelope contact__icon"></i>

        <div>
          <h3 class="contact__title">Email Me</h3>
          <span class="contact__subtitle">johnsteven.tapican@gmail.com</span>
        </div>
      </div>
    </div>

    <form action="" class="contact__form grid">
      <div class="contact__inputs grid">
        <div class="contact__content">
          <label for="" class="contact__label">Name</label>
          <input type="text" class="contact__input">
        </div>
      </div>
    </form>
  </div>
</section>
```

Preview.
![](/readme-img/Contact2.png)

3. Add another input field for email, project and message.
```
<!--==================== CONTACT ME ====================-->
<section class="contact section" id="contact">
  <h2 class="section__title">Contact Me</h2>
  <span class="section__subtitle">Get in Touch</span>

  <div class="contact__container container grid">
    <div>
      <div class="contact__information">
        <i class="uil uil-envelope contact__icon"></i>

        <div>
          <h3 class="contact__title">Email Me</h3>
          <span class="contact__subtitle">johnsteven.tapican@gmail.com</span>
        </div>
      </div>
    </div>

    <form action="" class="contact__form grid">
      <div class="contact__inputs grid">
        <div class="contact__content">
          <label for="" class="contact__label">Name</label>
          <input type="text" class="contact__input">
        </div>
        <div class="contact__content">
          <label for="" class="contact__label">Email</label>
          <input type="email" class="contact__input">
        </div>
      </div>
      <div class="contact__content">
        <label for="" class="contact__label">Project</label>
        <input type="text" class="contact__input">
      </div>
      <div class="contact__content">
        <label for="" class="contact__label">Message</label>
        <textarea name="" id="" cols="0" rows="7" class="contact__input"></textarea>
      </div>

      <div>
        <a href="#" class="button button--flex">
          Send Message
          <i class="uil uil-message button__icon"></i>
        </a>
      </div>
    </form>
  </div>
</section>
```

Preview.
![](/readme-img/Contact3.png)

### /assets/css/styles.css
1.  Add styling for our contact info.
```
/*==================== CONTACT ME ====================*/
.contact__container{
  row-gap: 3rem;
}

.contact__information{
  display: flex;
  margin-bottom: var(--mb-2);
}

.contact__icon{
  font-size: 2rem;
  color: var(--first-color);
  margin-right: var(--mb-0-75);
}

.contact__title{
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
}

.contact__subtitle{
  font-size: var(--small-font-size);
  color: var(--text-color-light);
}

.contact__content{
  background-color: var(--input-color);
  border-radius: 0.5rem;
  padding: 0.75rem 1rem 0.25rem;
}

.contact__label{
  font-size: var(--smaller-font-size);
  color: var(--title-color);
}

.contact__input{
  width: 100%;
  background-color: var(--input-color);
  color: var(--text-color);
  font-family: var(--body-font);
  font-size: var(--normal-font-size);
  border: none;
  outline: none;
  padding: 0.25rem 0.5rem 0.5rem 0;
}
```

Preview.
![](/readme-img/Contact4.png)


## N. Footer
### index.html
1. Let's create a footer with our socials.
```
<!--==================== FOOTER ====================-->
<footer class="footer">
  <div class="footer__bg">
    <div class="footer__container container grid">
      <div>
        <h1 class="footer__title">Steven</h1>
        <span class="footer__subtitle">Fullstack RPA Developer</span>
      </div>

      <ul class="footer__links">
        <li>
          <a href="#services" class="footer__link">Services</a>
        </li>
        <li>
          <a href="#portfolio" class="footer__link">Portfolio</a>
        </li>
        <li>
          <a href="#contact" class="footer__link">Contact Me</a>
        </li>
      </ul>

      <div class="footer__socials">
        <a href="https://www.facebook.com" target="_blank" class="footer__social">
          <i class="uil uil-facebook-f"></i>
        </a>
        <a href="https://www.instagram.com" target="_blank" class="footer__social">
          <i class="uil uil-instagram"></i>
        </a>
        <a href="https://www.twitter.com" target="_blank" class="footer__social">
          <i class="uil uil-twitter-alt"></i>
        </a>
      </div>
    </div>
  </div>
</footer>
```

Preview.
![](/readme-img/Footer1.png)

### /assets/css/styles.css
1. Add styling for our footer.
```
/*==================== FOOTER ====================*/
.footer{
  padding-top: 2rem;
}

.footer__container{
  row-gap: 3.5rem;
}

.footer__bg{
  background-color: var(--first-color-second);
  padding: 2rem 0 3rem;
}

.footer__title{
  font-size: var(--h1-font-size);
  margin-bottom: var(--mb-0-25);
}

.footer__subtitle{
  font-size: var(--small-font-size);
}

.footer__link{
  display: flex;
  flex-direction: column;
  row-gap: 1.5rem;
}

.footer__link:hover{
  color: var(--first-color-lighter);
}

.footer__social{
  font-size: 1.25rem;
  margin-right: var(--mb-1-5);
}

.footer__social:hover{
  color: var(--first-color-lighter);
}

.footer__copy{
  font-size: var(--smaller-font-size);
  text-align: center;
  color: var(--text-color-light);
  margin-top: var(--mb-3);
}

.footer__title,
.footer__subtitle,
.footer__link,
.footer__social{
  color: #FFF;
}
```

## O. Scroll
### /assets/js/main.js
1. Add the ff code block.
```
/*==================== SCROLL SECTIONS ACTIVE LINK ====================*/
const sections = document.querySelectorAll('section[id]')

function scrollActive(){
    const scrollY = window.pageYOffset

    sections.forEach(current =>{
        const sectionHeight = current.offsetHeight
        const sectionTop = current.offsetTop - 50;
        sectionId = current.getAttribute('id')

        if(scrollY > sectionTop && scrollY <= sectionTop + sectionHeight){
            document.querySelector('.nav__menu a[href*=' + sectionId + ']').classList.add('active-link')
        }else{
            document.querySelector('.nav__menu a[href*=' + sectionId + ']').classList.remove('active-link')
        }
    })
}
window.addEventListener('scroll', scrollActive)
```

### /assets/css/styles.css
1. Add some styling.
```
/* Active link */
.active-link{
  color: var(--first-color);
}
```

### index.html
1. Add an "active-link" class in our header.
This will highlight the current section we are in in the nav menu..
```
<!--==================== HEADER ====================-->
<header class="header" id="header">
  <nav class="nav container">
    <a href="#" class="nav__logo">Steven</a>

    <div class="nav__menu" id="nav-menu">
      <ul class="nav__list grid">
        <li class="nav__item">
          <a href="#home" class="nav__link active-link">
            <i class="uil uil-estate nav__icon"></i> Home
          </a>
        </li>
        <li class="nav__item">
          <a href="#about" class="nav__link">
            <i class="uil uil-user nav__icon"></i> About
          </a>
        </li>
        <li class="nav__item">
          <a href="#skills" class="nav__link">
            <i class="uil uil-file-alt nav__icon"></i> Skills
          </a>
        </li>
        <li class="nav__item">
          <a href="#services" class="nav__link">
            <i class="uil uil-briefcase-alt nav__icon"></i> Services
          </a>
        </li>
        <li class="nav__item">
          <a href="#portfolio" class="nav__link">
            <i class="uil uil-scenery nav__icon"></i> Portfolio
          </a>
        </li>
        <li class="nav__item">
          <a href="#contact" class="nav__link">
            <i class="uil uil-message nav__icon"></i> Contact Me
          </a>
        </li>
      </ul>
      <i class="uil uil-times nav__close" id="nav-close"></i>
    </div>

    <div class="nav__btns">
      <div class="nav__toggle" id="nav-toggle">
        <i class="uil uil-apps"></i>
      </div>
    </div>
  </nav>
</header>
```

Preview.
![](/readme-img/Scroll1.png)

## P. Change Background Header
### /assets/js/main.js
```
/*==================== CHANGE BACKGROUND HEADER ====================*/
function scrollHeader(){
    const nav = document.getElementById('header')
    // When the scroll is greater than 200 viewport height, add the scroll-header class to the header tag
    if(this.scrollY >= 80) nav.classList.add('scroll-header'); else nav.classList.remove('scroll-header')
}
window.addEventListener('scroll', scrollHeader)
```

### /assets/css/styles.css
```
/* Change background header */
.scroll-header{
  box-shadow: 0 -1px 4px rgba(0, 0, 0, 0.15);
}
```

## Q. SCROLL TOP
### index.html
1. Get an 'arrow-up' from Iconscout and add the ff class on it.
```
<!--==================== SCROLL TOP ====================-->
<a href="#" class="scrollup" id="scroll-up">
  <i class="uil uil-arrow-up scrollup__icon"></i>
</a>
```

### /assets/css/styles.css
```
/*========== SCROLL UP ==========*/
.scrollup{
  position: fixed;
  right: 1rem;
  bottom: -20%;
  background-color: var(--first-color);
  opacity: 0.8;
  padding: 0 0.3rem;
  border-radius: 0.4rem;
  z-index: var(--z-tooltip);
  transition: 0.4s;
}

.scrollup:hover{
  background-color: var(--first-color-alt);
}

.scrollup__icon{
  font-size: 1.5rem;
  color: #FFF;
}

/* Show scroll */
.show-scroll{
  bottom: 5rem;
}
```

### /assets/js/main.js
```
/*==================== SHOW SCROLL UP ====================*/
function scrollUp(){
    const scrollUp = document.getElementById('scroll-up');
    // When the scroll is higher than 560 viewport height, add the show-scroll class to the a tag with the scroll-top class
    if(this.scrollY >= 560) scrollUp.classList.add('show-scroll'); else scrollUp.classList.remove('show-scroll')
}
window.addEventListener('scroll', scrollUp)
```

Preview.
![](/readme-img/Scroll2.png)

## R. DARK/LIGHT Theme
### index.html
1. Now let's add dark/light mode. We can get the moon icon from Iconscout.
```
<!-- Theme change button -->
<i class="uil uil-moon change-theme" id="theme-button"></i>
```

### /assets/css/styles.css
1. Next we add some styling.
```
/*========== Variables Dark theme ==========*/
body.dark-theme{
  /* HSL color mode */
  --first-color-second: hsl(var(--hue-color), 30%, 8%);
  --title-color: hsl(var(--hue-color), 8%, 95%);
  --text-color: hsl(var(--hue-color), 8%, 75%);
  --input-color: hsl(var(--hue-color), 29%, 16%);
  --body-color: hsl(var(--hue-color), 28%, 12%);
  --container-color: hsl(var(--hue-color), 29%, 16%);

}

/*========== Button Dark/Light ==========*/
.nav__btns{
  display: flex;
  align-items: center;
}

.change-theme{
  font-size: 1.25rem;
  color: var(--title-color);
  margin-right: var(--mb-1);
  cursor: pointer;
}

.change-theme:hover{
  color: var(--first-color);
}
```

Preview.
![](/readme-img/Dark1.png)

### /assets/js/main.js
1. This js will let us switch from dark to light mode and vice versa.
```
/*==================== DARK LIGHT THEME ====================*/
const themeButton = document.getElementById('theme-button')
const darkTheme = 'dark-theme'
const iconTheme = 'uil-sun'

// Previously selected topic (if user selected)
const selectedTheme = localStorage.getItem('selected-theme')
const selectedIcon = localStorage.getItem('selected-icon')

// We obtain the current theme that the interface has by validating the dark-theme class
const getCurrentTheme = () => document.body.classList.contains(darkTheme) ? 'dark' : 'light'
const getCurrentIcon = () => themeButton.classList.contains(iconTheme) ? 'uil-moon' : 'uil-sun'

// We validate if the user previously chose a topic
if (selectedTheme) {
  // If the validation is fulfilled, we ask what the issue was to know if we activated or deactivated the dark
  document.body.classList[selectedTheme === 'dark' ? 'add' : 'remove'](darkTheme)
  themeButton.classList[selectedIcon === 'uil-moon' ? 'add' : 'remove'](iconTheme)
}

// Activate / deactivate the theme manually with the button
themeButton.addEventListener('click', () => {
    // Add or remove the dark / icon theme
    document.body.classList.toggle(darkTheme)
    themeButton.classList.toggle(iconTheme)
    // We save the theme and the current icon that the user chose
    localStorage.setItem('selected-theme', getCurrentTheme())
    localStorage.setItem('selected-icon', getCurrentIcon())
})
```

Preview.
![](/readme-img/Dark2.png)

## S. SCROLL BAR
### /assets/css/styles.css
1. Update the main code for HSL.
```
/*==================== VARIABLES CSS ====================*/
:root { /* We use :root so style can be applied globally. */
    --header-height: 3rem;

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
    --scroll-bar-color: hsl(var(--hue-color), 12%, 99%);
    --scroll-thumb-color: hsl(var(--hue-color), 12%, 80%);
```

2. Let's add some styling for our scroll bar.
```
/*========== SCROLL BAR ==========*/
::-webkit-scrollbar{
  width: .60rem;
  background-color: var(--scroll-bar-color);
  border-radius: 0.5rem;
}

::-webkit-scrollbar-thumb{
  background-color: var(--scroll-thumb-color);
  border-radius: .5rem;
}

::-webkit-scrollbar-thumb:hover{
  background-color: var(--text-color-light);
}
```

3. Update our dark theme variables. This will apply dark/light mode in our scroll bar.
```
/*========== Variables Dark theme ==========*/
body.dark-theme{
  /* HSL color mode */
  --first-color-second: hsl(var(--hue-color), 30%, 8%);
  --title-color: hsl(var(--hue-color), 8%, 95%);
  --text-color: hsl(var(--hue-color), 8%, 75%);
  --input-color: hsl(var(--hue-color), 29%, 16%);
  --body-color: hsl(var(--hue-color), 28%, 12%);
  --container-color: hsl(var(--hue-color), 29%, 16%);
  --scroll-bar-color: hsl(var(--hue-color), 12%, 48%);
  --scroll-thumb-color: hsl(var(--hue-color), 12%, 36%);
}
```


## T.
Preview.
![](/readme-img/Dark2.png)
