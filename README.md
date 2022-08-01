# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Frontend Mentor - NFT preview card component solution](#frontend-mentor---nft-preview-card-component-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
      - [Mobile View](#mobile-view)
      - [Desktop View](#desktop-view)
  - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Useful resources](#useful-resources)
  - [Author](#author)
  - [Acknowledgments](#acknowledgments)

---
## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover & active states for interactive elements

---
### Screenshot

#### Mobile View
<img src="images/mobileView.png" alt="drawing" width="40%"/>


#### Desktop View
<img src="images/desktopView.png" alt="drawing" width="100%"/>

---

## Links

- Solution URL: [Github Code](https://github.com/VLOrozco/Mobile-first-cssFlexbox-nft-preview-card-component.git)
- Live Site URL: [NFT preview card component](https://vlorozco.github.io/Mobile-first-cssFlexbox-nft-preview-card-component/)

---
## My process

### Built with

- HTML5
- CSS Animation
- CSS Flexbox
- Mobile-first workflow


### What I learned
Updated Monday, August 1, 2022 |
*Thank you to [Vanza Setia](https://www.frontendmentor.io/profile/vanzasetia) for your help.*


**Index.html preparation for images hover solution:**

```html
<!-- IMAGES -->
<div id="image" role="img">
  <img id="equilibrium" src="/images/image-equilibrium.jpg" alt="NFT equilibrium image">
  <div id="active-images">
    <div class="overlay"></div>
    <img id="eye" src="/images/icon-view.svg" alt="Image of an eye icon">
  </div>
</div>
```

**Updated style.css solution for hovered NFT card images with rotation animation included:**

```css
/* NFT CARD IMAGES | LAYOUT */
#active-images {
  width: 100%;
  height: 100%;
  margin-top: -18.8rem;
  position: relative;
  display: flex;
  cursor: pointer;
  opacity: 0;
  transition: transform 3s;
}
  /* IMAGE HOVER & ACTIVE STATE */
  #image:hover #active-images {
    transform: rotateY(180deg);
    opacity: 1;
  }
```

---
Thursday, June 9, 2022 |
*The first challenge I encountered was accurately positioning the elements of .image & .view-img / .eye as an overlay.*

**my index.html solution in preparation to apply styles.css:**
```html
<!-- IMAGE -->
  <div class="image">
    <img src="images/image-equilibrium.jpg" alt="equilibrium image myImg" class="equilibrium">
    
    <div class="hide show">
      <div class="view-img"></div>
      <img src="images/icon-view.svg" alt="eye view icon" class="eye">
    </div>
  </div>
```

**my styles.css solution for positioning the elements layered:**
```css
/* NFT CARD IMAGES | LAYOUT */
#active-images {
  width: 100%;
  height: 100%;
  margin-top: -18.8rem;
  position: relative;
  display: flex;
  cursor: pointer;
  opacity: 0;
}
  .overlay {
    width: 278px;
    height: 278px;
    position: absolute;
    background-color: rgb(0, 255, 247);
    border-radius: 8px;
    opacity: 0.5;
    mix-blend-mode: normal;
  }
  #eye {
    width: 48px;
    height: 48px;
    margin: auto;
    z-index: 5;
  }
```

*Lastly, it was challenging to hide and show the .img-view & .eye elements for their corresponding hover || active states.*

**my styles.css solution to hide/show an image in the hover/active states:**
```css
/* ACTIVE STATE */
.equilibrium:hover {
  cursor: pointer;
}
.equilibrium:active + .show {
  cursor: pointer;
  visibility: visible;
}
```

---

### Useful resources

- [W3schools - css display property](https://www.w3schools.com/cssref/pr_class_display.asp) - Just a friendly reminder for css display properties. This helped me in discovering the solution to overlay the image elements.
  
- [W3schools - display element hover](https://www.w3schools.com/howto/howto_css_display_element_hover.asp) - This helped me in creating a solution to hide/show the image elements. I really liked this pattern as it helped me with my solution and introduced me to the (+) adjacent sibling selector which will come in handy in future code.

---

## Author

- VLOrozco Portolio Website - [Veronica L. Orozco](https://vlorozco.com)
- Github - [Veronica L. Orozco](https://github.com/VLOrozco)
- Frontend Mentor - [@VLOrozco](https://www.frontendmentor.io/profile/VLOrozco)
- Codecademy - [orozcov3](https://www.codecademy.com/profiles/orozcoV3)

---
## Acknowledgments

Thank you to [Vanza Setia](https://www.frontendmentor.io/profile/vanzasetia), Frontend Mentor Community Member, for your support in helping me find a solution to my hover bug and enhancing my README.md file by sharing a link to [Github Docs for Syntax highlighting](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks). I appreciate your support and time sharing your knowledge with me. I look forward to reviewing your code for inspiration and more learning in markdown and coding!