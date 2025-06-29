# Frontend Mentor - Fylo data storage component solution

This is a solution to the [Fylo data storage component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/fylo-data-storage-component-1dZPRbV5n). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

![Desktop](/images/solution-screenshot-desktop.png)
![Mobile](/images/solution-screenshot-mobile.png)

### Links

- Solution URL: [https://github.com/HaiDangN/fylo-data-storage-component]
- Live Site URL: [https://haidangn.github.io/fylo-data-storage-component/](https://haidangn.github.io/fylo-data-storage-component)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

I learned how to create a tiny component shape that sticks out of another component like the triangle that comes out of the white indicator box. First, you can apply `::after` to the component and then this is also how you make a triangle. Essentially make the height and width 0, and then the borders stick out diagonally from the point.

```css
.storage-ui__remaining-storage::after {
    content: "";
    position: absolute;
    bottom: -22px;      
    right: 0;       

    width: 0;
    height: 0;
    border-left: 12px solid transparent;
    border-right: 12px solid white;
    border-top: 12px solid white;
    border-bottom: 12px solid transparent;
}
```

I learned that `top` means how many units does the bottom of the current element go underneath the top of the parent container.

You can use `transform` to move an element within units of its own width and height:

```css
    transform: translateY(-66%);
```

I learned that `background-size: cover` scales the image so that it is able to cover the ENTIRE element. If you want it to stretch horizontally, you can use `background-size: 100% auto;`
