<div align="center">
  <img 
    src="Product card desktop.png"
    alt="Product card for CHANEL Gabrielle Essence Eau De Parfum"
    height="350px">
</div>

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa).  

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements
- Extra challenge: view the optimal image based on device screen size (responsive images)

I noticed the source files included both a full-sized image for desktop and a cropped image for mobile, so I added an extra challenge for myself to use responsive images.

<div align="center">
  <img
    src="Product card desktop.png"
    alt="Product card for CHANEL Gabrielle Essence Eau De Parfum, desktop version horizontal display with image on the left and product description, pricing, and add to cart button on the right"
    height="350px">
  <img 
    src="Product card mobile.png"
    alt="Product card for CHANEL Gabrielle Essence Eau De Parfum, mobile version vertical display with image on top and product description, pricing, and add to cart button on bottom"
    height="350px">
  <p><em>Desktop (horizontal) and mobile (vertical) designs</em></p>
</div>

### Links

- Solution URL: [Product preview card](https://rileydevdzn.github.io/fluid-images-picture-element/)

## My process

### Built with

- Semantic HTML5 markup
- Responsive images with the `<picture>` element
- CSS variables
- Flexbox
- Responsive design
- Realistic workflow, building from professional Figma design files (design-to-code) 

### What I learned

I experimented with two solutions for responsive images in this project: the first using `srcset` and `sizes` attributes on the `<img>` element, and the second using the `<picture>` element. I worked with both to investigate the pros and cons of each approach. Sometimes as developers we have to work within constraints where a specific method might be unavailable; understanding which methods work best in which situations and being able to provide alternatives is a valuable skill.

The better solution for this project was using the `<picture>` element, so that I could serve a cropped image on mobile and the full-sized image on desktop.

```html
<picture>
  <source srcset="./prodpreview-image-product-mobile.jpg" media="(max-width: 554px)"/>
  <source srcset="./prodpreview-image-product-desktop.jpg" media="(min-width: 555px)"/>
  <img class="product-card-img" src="./prodpreview-image-product-desktop.jpg" alt="Bottle of Gabrielle perfume from Chanel"/>
</picture>
```

Styling was a bit trickier. After digging into Stack Overflow, I realized I made a mistake when I initially targeted the `<picture>` element with my CSS, since the `<img>` element represents the actual presented image. I added a class to the `<img>` element and was able to style as needed.   

### Continued development

I found both responsive image solutions were useful for this project, but the `<picture>` element was better suited for serving cropped vs. full-sized images in this case. I'd like to explore using the `srcset` and `sizes` attributes on the `<img>` element on a future project. I'll continue focusing on responsive design in future projects to find better, more efficient, and more effective approaches to improve my skills.

### Useful resources

- [MDN Web Docs: Responsive images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images) - This helped me understand the different methods available for responsive images and best use-cases for each, with examples. 
- [Stack Overflow: Applying CSS style to the picture element](https://stackoverflow.com/questions/69853065/apply-css-style-only-to-the-loaded-image-frompicture-element) - Stack Overflow is one of my go-to resources when I'm trying to figure out why something isn't working as I expect.   

## Author

- Frontend Mentor - [@rileydevdzn](https://www.frontendmentor.io/profile/rileydevdzn)
