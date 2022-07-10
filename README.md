# Responsive Webpage /Flexbox /JS

This is a webpage built using Flexbox & JS.

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)


## Overview

This goal of this project is to develop a simple webpage having a responsive
navigation using Flexbox and JS.


### Screenshot

[screenshot of webpage](img/screenshot.png)


### Links

- [Live site URL](https://itachidorri.github.io/responsive-webpage-flexbox/)


## My process
1. Building the html structure for the project using references.
2. Adding CSS.
3. Finding solution to errors on google, documentations & developer communities.
4. Implementing solutions.


### Built with

- Semantic HTML5 markup
- CSS custom properties
- [Font stack](https://www.cssfontstack.com/) - For font stacks
- vanilla JS


### What I learned

To build a responsive navigation using JS:
1. Data attributes - It was used as a switch(like a light switch) to toggle the navigation items in and out of the navigation button. This was achieved in the following ways:

  ```html
  <nav data-visible="false" class="primary-navbar flex">
  ```

  ```css
  .primary-navbar{
    transform: translateX(100%);
  }
  ```

  Here, the data attribute "data-visible" was set to "False" when the Navigation
  was moved outside the viewport using CSS as you can see in the code snippet above. Then, when "data-visible" was set to 'True', the CSS below toggled the navigation back into the screen.

  ```css
  .primary-navbar[data-visible="true"]{
    transform: translateX(0%);
  }
  ```

  ```js
  navToggle.addEventListener('click',() => {
    const visibility = primaryNav.getAttribute("data-visible");
    console.log(visibility);

    if (visibility ==="false"){
      primaryNav.setAttribute('data-visible',true);
    }

    else if (visibility ==="true") {
      primaryNav.setAttribute('data-visible',false);
    }
  })
  ```

  Finally after writing some JS, a responsive navigation was built

New CSS properties:
1. z-index: sets stack order of elements and an element with greater stack order is always in front of an element with a lower stack order.
2. .'class':nth-child('order number of child class'){} - This allows you to
  select all child classes of a parent.


### Continued development

To gain proper understanding of flexbox, vanilla javascript and responsive
design.


### Useful resources

- [Font stack](https://www.cssfontstack.com/) - For font stacks
- [Stack developer](https://stackoverflow.com/) - Community of tech professionals, where you'll probably find answers to your project obstacles or errors.
- [Kevin powell](https://www.youtube.com/kepowob) - My guy has helped me
understand HTML & CSS very easily. Do check him out!


## Author

- Frontend Mentor - [@Itachidorri](https://www.frontendmentor.io/profile/Itachidorri)
- Github - [Itachidorri](https://github.com/Itachidorri)


## Acknowledgments

I want to express my gratitude to developer communities such as "stackoverflow" & developers such as 'kevin powell' who have helped me progress in my developer journey with tutorials, solutions and useful resources. Hare Krishna!
