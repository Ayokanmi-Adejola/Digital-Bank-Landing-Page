# Frontend Mentor - Easybank Landing Page Solution

This is a solution to the [Easybank landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/easybank-landing-page-WaUhkoDN). Frontend Mentor challenges help you improve your coding skills by building realistic projects.


## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page
- Navigate using a mobile menu on smaller screens

### Screenshot

![Easybank Landing Page Screenshot](./design/desktop-preview.jpg)


## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- Vanilla JavaScript for mobile menu toggle

### What I learned

This project was a great opportunity to practice creating a responsive landing page with a modern design. 

Some key learnings include:

- Creating a responsive navigation menu that transforms into a mobile menu on smaller screens
- Implementing a hero section with overlapping elements and background patterns
- Using CSS Grid for responsive card layouts
- Working with SVG icons and optimizing images
- Creating smooth hover effects and transitions

Here are some code snippets I'm particularly proud of:

```css
/* Hero section with background positioning */
.hero::before {
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
  background-image: url('../images/bg-intro-mobile.svg');
  background-size: cover;
  background-position: center top;
  background-repeat: no-repeat;
}

/* Desktop hero section with proper image positioning */
@media (min-width: 768px) {
  .hero::before {
    background-image: url('../images/bg-intro-desktop.svg');
    background-position: 0% 70%;
    background-size: 130%;
    left: 45%;
    width: 150%;
  }

  .hero__container {
    display: flex;
    flex-direction: row;
    align-items: center;
    padding-top: 0;
    text-align: left;
  }

  .hero__image img {
    position: absolute;
    width: 120%;
    max-width: none;
    transform: translate(-10%, -12%);
    right: -10%;
  }
}
```

```javascript
// Mobile menu toggle functionality
document.addEventListener('DOMContentLoaded', function() {
  const toggle = document.querySelector('.header__toggle');
  const menu = document.querySelector('.header__menu');
  const body = document.querySelector('body');

  toggle.addEventListener('click', function() {
    // Toggle menu visibility
    menu.classList.toggle('active');
    toggle.classList.toggle('active');

    // Prevent scrolling when menu is open
    body.classList.toggle('no-scroll');
  });
});
```

### Continued development

In future projects, I would like to focus on:

- Implementing more advanced animations and transitions
- Improving accessibility features
- Optimizing performance further
- Exploring CSS frameworks like Tailwind CSS
- Adding more interactive elements with JavaScript

## Author

- Frontend Mentor - [@Ayokanmi-Adejola](https://www.frontendmentor.io/profile/Ayokanmi-Adejola)
