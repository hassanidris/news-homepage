# Frontend Mentor - News homepage solution

This is a solution to the [News homepage challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/news-homepage-H6SWTa1MFl). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### Screenshot

![](./screenshot.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- SASS / CSS Variables
- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

- CSS Variables

```scss
:root {
  //  ### Primary
  --clr-prm-400-softOrange: hsl(35, 77%, 62%);
  --clr-prm-400-softRed: hsl(5, 85%, 63%);

  //  ### Neutral
  --clr-nut-100-offWhite: hsl(36, 100%, 99%);
  --clr-nut-200-grayishBlue: hsl(233, 8%, 79%);
  --clr-nut-600-darkGrayishBlue: hsl(236, 13%, 42%);
  --clr-nut-900-veryDarkBlue: hsl(240, 100%, 5%);

  //  ## Typography
  --ff-inter: "Inter", sans-serif;

  --fw-normal: 400;
  --fw-bold: 700;
  --fw-extraBold: 800;

  --fs-400: 0.9375rem; // body font
  --fs-500: 1rem; // buttons font
  --fs-600: 1.125rem; // h4
  --fs-700: 1.25rem; // h3
  --fs-800: 1.9rem; // h2
  --fs-900: 2.5rem; // h1
}
```

- Nesting media queries inside the classes

```scss
.showcase {
  @media (min-width: 768px) {
    grid-column: 1 / span 2;
  }

  &__content {
    margin: 1.25rem 0;

    @media (min-width: 768px) {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 2rem;
    }
  }

  &__title {
    font-size: var(--fs-900);
    font-weight: var(--fw-extraBold);
    color: var(--clr-nut-900-veryDarkBlue);
  }

  &__desc {
    margin-bottom: 1rem;
    color: var(--clr-nut-600-darkGrayishBlue);
  }

  &__btn {
    background-color: var(--clr-prm-400-softRed);
    color: var(--clr-nut-100-offWhite);
    font-size: var(--fs-500);
    padding: 0.8rem 2rem;
    border: none;
    outline: none;
    text-transform: uppercase;
    letter-spacing: 0.2rem;
    font-weight: var(--fw-bold);
    transition: all 0.3s ease-in-out;

    &:hover {
      background-color: var(--clr-nut-900-veryDarkBlue);
      cursor: pointer;
    }
  }
}
```

- Vanilla Javascript for menu in mobile

```js
const navbar = document.querySelector("nav");
const openMenu = document.getElementById("menu-btn");
const closeMenu = document.getElementById("menu-close");

openMenu.addEventListener("click", () => {
  navbar.classList.add("open");
});

closeMenu.addEventListener("click", () => {
  navbar.classList.remove("open");
});
```

## Author

- Github - [hassanidris](https://github.com/hassanidris)
- Frontend Mentor - [@hassanidris](https://www.frontendmentor.io/profile/hassanidris)
