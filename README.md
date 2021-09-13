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
