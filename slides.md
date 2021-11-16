---
theme: ./theme
class: text-center
highlighter: prism
lineNumbers: true
info: |
  ## Slides for Intro to SVG L&L
drawings:
  persist: false
download: true
layout: intro
title: Intro to SVG
---

# Intro to SVG


<div>
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Let's start <carbon:arrow-right class="inline"/>
  </span>
</div>


---
layout: presenter
presenterImage: 'https://pbs.twimg.com/profile_images/1441783883456942080/vV37mSqv_400x400.jpg'
---

# Estee Tey

- 💻 Grad Software Developer at Thoughtworks
- ✏ Writes about Web Dev, UI, Dev growth
- 🎨 Experienced in creating mockups & graphics

<div class="my-10 grid grid-cols-[80px,1fr]">
  <div><ri-github-line class="opacity-50"/><a href="https://github.com/lyqht" target="_blank">lyqht</a></div>
  <div><ri-twitter-line class="opacity-50"/><a href="https://twitter.com/estee_tey" target="_blank">estee_tey</a></div>
</div>

---

# Expectations

<div class='grid grid-cols-2 grid-rows-2 gap-20'>
  <div v-click>
    <h2>No Prerequisites</h2>
    <code>expect(target_audience).toBeAny()</code>
  </div>
  <div v-click>
    <h2>Your time to be worth it</h2>
    <code>expect(🍚⏱).toYield(✅)</code>
  </div>
  <div v-click>
    <h2>Learn something</h2>
    <code>expect(🧠).toIncrease();</code>
  </div>
  <div v-click>
    <h2>Have fun thinking</h2>
    <code>expect(🤔).andThen(😄)</code>
  </div>

</div>

---

# Table of Contents

1. What is SVG?
2. Why do we use SVG?
3. How do we get SVG?
4. How to use SVG?

---
layout: center
class: text-center
---

# What is SVG?

---
layout: center
class: text-center
---

# Images

<div>
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Story Time! <carbon:arrow-right class="inline"/>
  </span>
</div>

---

<div class="grid grid-cols-2">
<img v-click src="https://i.etsystatic.com/10236183/c/1599/1271/170/109/il/fd287d/2254910083/il_340x270.2254910083_srgv.jpg" />
<img v-click src="/story-raster-vs-vector/telegram_chat.png" />
</div>

---

<div class="grid grid-cols-2">
<img v-click src="/story-raster-vs-vector/draft1.jpg" />
<img v-click src="/story-raster-vs-vector/draft2.jpg" />
</div>

---

<img class="h-80 mx-auto" src="/story-raster-vs-vector/draft_done.jpg" />


---

<div class="grid grid-cols-2">

<img v-click src="/story-raster-vs-vector/design.png" />
<img v-click src="/story-raster-vs-vector/design_colored.png" />

</div>
---

<img src="/story-raster-vs-vector/design_final.png" />

---

# Raster vs Vector Images

![raster vs vector images](https://vector-conversions.com/images/vector_vs_raster.jpg)

---

# Image File Types

| File Extension                          | Description                                                      |
| --------------------------------------- | ---------------------------------------------------------------- |
| <code>.gif</code>                       | Graphics Interchange Format                                      |
| <code>.png</code>                       | Portable Network Graphic                                         |
| <code>.jpg</code>  / <code>.jpeg</code> | Image format by Joint Photographic Experts Group                 |
| <code>.webp</code>                      | A superior image format of <code>.png</code> & <code>.jpg</code> |
| <code>.svg</code>                       | Scalable Vector Graphics                                         |

---

# Image File Types

| File Extension                          | Color Modes                                            | Compression                 | Usage                                                            |
| --------------------------------------- | ------------------------------------------------------ | --------------------------- | ---------------------------------------------------------------- |
| <code>.gif</code>                       | Indexed Color                                          | Lossless                    | Animated images                                                  |
| <code>.png</code>                       | Greyscale, True Color, Alpha                           | Lossless (better than .GIF) | Static Line art, iconic graphics where transparency matters.     |
| <code>.jpg</code>  / <code>.jpeg</code> | True Color                                             | Lossy                       | Photographs, realistic images of people, venues etc.             |
| <code>.webp</code>                      | Depends on compression                                 | Lossless / Lossy            | A superior image format of <code>.png</code> & <code>.jpg</code> |
| <code>.svg</code>                       | Anything that can be specified using CSS color syntax. | NA                          | UI that requires to be redrawn accurately at different sizes     |


<!-- Compression: The information that is discarded in the compression is information that the human eye cannot detect -->

---

# How to get SVG

1. Create SVG from scratch
2. Generate SVG
3. Extract from websites

---
layout: center
class: text-center
---

# Create SVG with 3 basic elements

`<rectangle />`

`<circle />`

`<polygon />`

<div class="pt-12" v-click>
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Code Time! <carbon:arrow-right class="inline"/>
  </span>
</div>

---

# Create SVG with 3 simple shapes in code

<img class="h-80" src="https://waytogo.s3.ap-southeast-1.amazonaws.com/wp-content/uploads/2016/06/28170410/G-A-montage-of-flag-erasers.jpg" />


---
layout: new-section
logoHeader: '/intro-to-svg-slides/terminal-box-fill.svg'
---

# JP flag in SVG 

<div class="demo-container">
  <svg class="demo-svg">
      <rect width="100%" height="100%" fill="white" />
      <circle cx="50%" cy="50%" r=60 fill="#BC002D" />
  </svg>
</div>

<div class='demo-container' v-click>

```html {all}
<svg>
    <rect width="100%" height="100%" fill="white" />
    <circle cx="50%" cy="50%" r=60 fill="#BC002D" />
</svg>
```
  
</div>


---
layout: new-section
logoHeader: '/intro-to-svg-slides/terminal-box-fill.svg'
---

# TH flag in SVG

<div class="demo-container">
  <svg class="demo-svg">
    <rect width="100%" height="20%" y="0" fill="red" />
    <rect width="100%" height="20%" y="20%" fill="white" />
    <rect width="100%" height="20%" y="40%" fill="blue" />
    <rect width="100%" height="20%" y="60%" fill="white" />
    <rect width="100%" height="20%" y="80%" fill="red" />
  </svg>
</div>

<div class='demo-container' v-click>

```html {all}
<svg>
    <rect width="100%" height="20%" y="0" fill="red" />
    <rect width="100%" height="20%" y="20%" fill="white" />
    <rect width="100%" height="20%" y="40%" fill="blue" />
    <rect width="100%" height="20%" y="60%" fill="white" />
    <rect width="100%" height="20%" y="80%" fill="red" />
</svg>
```
  
</div>

---
layout: new-section
logoHeader: '/intro-to-svg-slides/terminal-box-fill.svg'
---

# VN flag in SVG 

<div class="demo-container">
  <svg class="demo-svg">
    <defs>
      <polygon id="star" fill="yellow"
        points="100,10 40,198 190,78 10,78 160,198" />
    </defs>
    <rect width="100%" height="100%" fill="red" />
    <svg viewBox="100 0 600 600" x="25%" y="25%">
      <use href="#star">
      </use>
    </svg>
  </svg>
</div>

<div class='demo-container' v-click>

```html {all}
<svg>
  <defs>
    <polygon id="star" fill="yellow"
      points="100,10 40,198 190,78 10,78 160,198" />
  </defs>
  <rect width="100%" height="100%" fill="red" />
  <svg viewBox="100 0 600 600" x="25%" y="25%">
    <use href="#star">
    </use>
  </svg>
</svg>
```
  
</div>

---
layout: new-section
logoHeader: '/intro-to-svg-slides/terminal-box-fill.svg'
---

## Polygon vs Polyline

<div class='grid-cols-2 grid'>

<div class="demo-container">
  <svg class="demo-svg">
    <defs>
      <polygon id="polygon" points="100,10 40,198 190,78 10,78 160,198"  fill='#abcbca' stroke='#123123' stroke-width='5'  />
    </defs>
    <svg viewBox="100 0 300 300" x="25%" y="25%">
      <use href="#polygon">
      </use>
    </svg>
  </svg>

```html {all}
<polygon points="100,10 40,198 190,78 10,78 160,198" fill='#abcbca' stroke='#123123' stroke-width='5'  />
```


</div>

<div class="demo-container">
  <svg class="demo-svg">
    <defs>
      <polyline id="polyline" points="100,10 40,198 190,78 10,78 160,198"  fill='#abcbca' stroke='#123123' stroke-width='5'  />
    </defs>
    <svg viewBox="100 0 300 300" x="25%" y="25%">
      <use href="#polyline">
      </use>
    </svg>
  </svg>

```html {all}
<polyline points="100,10 40,198 190,78 10,78 160,198"  fill='#abcbca' stroke='#123123' stroke-width='5'  />
```

</div>




</div>


---
layout: new-section
logoHeader: '/intro-to-svg-slides/terminal-box-fill.svg'
---

# SG flag in SVG

<div class="demo-container">
  <svg class="demo-svg">
    <defs>
        <polygon id="white-star" points="100,10 40,198 190,78 10,78 160,198" fill="white" />
    </defs>
    <rect width="100%" height="50%" fill="red" />
    <rect width="100%" height="50%" y="50%" fill="white" />
    <circle cx='15%' cy='25%' r='30' fill='white' />
    <circle cx='20%' cy='25%' r='30' fill='red' />
    <svg viewBox="600 -100 1000 1800">
        <use href="#white-star" />
        <use href="#white-star" x="-20%" y="10%" />
        <use href="#white-star" x="20%" y="10%" />
        <use href="#white-star" x="-12.5%" y="22%" />
        <use href="#white-star" x="12.5%" y="22%" />
    </svg>
  </svg>
</div>

<div class='demo-container' v-click>

```svg {all}
<svg>
  <rect width="100%" height="50%" fill="red" />
  <rect width="100%" height="50%" y="50%" fill="white" />
  <circle cx='15%' cy='25%' r='30' fill='white' />
  <circle cx='20%' cy='25%' r='30' fill='red' />
  <svg viewBox="600 -100 1000 1800">
    <use href="#white-star" />
    <use href="#white-star" x="-20%" y="10%" />
    <use href="#white-star" x="20%" y="10%" />
    <use href="#white-star" x="-12.5%" y="22%" />
    <use href="#white-star" x="12.5%" y="22%" />
  </svg>
</svg>
```
  
</div>
---
layout: center
class: text-center
---

# Create SVG with Design Tools

<div class='mx-auto px-4 w-100 grid place-items-center grid-cols-3 gap-x-10'>
  <a href="https://www.figma.com"><img src="https://cdn.freebiesupply.com/logos/thumbs/2x/figma-1-logo.png" /></a>
  <a href="https://www.sketch.com/"><img src="https://cdn.iconscout.com/icon/free/png-256/sketch-61-722739.png" /></a>
  <a href="https://www.adobe.com/sg/products/illustrator.html"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fb/Adobe_Illustrator_CC_icon.svg/1200px-Adobe_Illustrator_CC_icon.svg.png" /></a>
</div>

<!-- TODO: try drawing gummy bear in Figma and exporting it as a file, then show how to use it as a developer  -->

---
layout: center
class: text-center
---

# Figma Demo

Ellipse,
Polygon,
Paths,
Bezier Curves

<a href="https://www.figma.com/file/vHcMllyWIi5lPMhKldSI7k/intro-to-svg-shapes"><img class="h-20 mx-auto" src="https://cdn.freebiesupply.com/logos/thumbs/2x/figma-1-logo.png" /></a>

<!-- Demo: bezier curve ear, adding triangle party hat -->

---
layout: new-section
logoHeader: '/intro-to-svg-slides/terminal-box-fill.svg'
---
# Setting SVG File as an image source

<div class='grid grid-cols-2'>
<img class='mx-auto' src="https://raw.githubusercontent.com/lyqht/intro-to-svg-slides/main/public/svg/animals/Rabbit.svg"/>

```html
<img src="/svg/animals/Rabbit.svg"/>
```
</div>

<!-- When you add an SVG image using the <img> tag without specifying the size, it assumes the size of the original SVG file. -->

---
layout: new-section
logoHeader: '/intro-to-svg-slides/terminal-box-fill.svg'
---
# Setting SVG File as an image source

<div class='grid grid-cols-2'>
<img class='mx-auto special-image' src="https://raw.githubusercontent.com/lyqht/intro-to-svg-slides/main/public/svg/animals/Rabbit.svg"/>
<div>

```html
<img src="/svg/animals/Rabbit.svg" 
  class="special-image" />
```

```css
.special-image {
  height:240px; 
  animation:spin 4s linear infinite;
}

@keyframes spin { 
  100% {
      transform:rotate(360deg); 
  } 
}
```

</div>


</div>

<style>
.special-image {
  height:240px; 
  animation:spin 4s linear infinite;
}

@keyframes spin { 
  100% {
      transform:rotate(360deg); 
  } 
}
</style>

<!-- When you add an SVG image using the <img> tag without specifying the size, it assumes the size of the original SVG file. -->

---

# Generate SVG

<div class="mx-auto h-80 grid grid-cols-2">
  <div>
    1. <a href="https://squircley.app/">Squicley</a> for generating Squircles
    <img class="mt-6 pr-6" src="/squircley-demo.png" />
  </div>
</div>

---

# Generate SVG

<div class="mx-auto h-80 grid grid-cols-2">
  <div>
    2. <a href="https://www.svgbackgrounds.com/">SVGBackgrounds.com</a> for generating backgrounds
    <img class="mt-6 pr-6" src="/SVGBackgrounds-demo.png" />
  </div>
</div>

---

# Extract from websites

Demo with [Hacktoberfest's SVG](https://hacktoberfest.digitalocean.com/)

> P.S. If you use any extracted images for your own websites or apps, please remember to give **attribution**.

---

# Bonus: Optimization of SVG

[SVGOMG](https://jakearchibald.github.io/svgomg/) 

---

# Bonus for React Devs: convert from SVG to JSX

[SVG to JSX Demo](https://svg2jsx.com/)

---

# Summary

1. What is SVG?
2. Why do we use SVG?
3. How do we get SVG?
4. How to use SVG?

---

# SVG Element Cheatsheet

|     | Shape     | Usage Example                                              |
| --- | --------- | ---------------------------------------------------------- |
| 1.  | Square    | `<rect width="40" height="40" />`                          |
| 2.  | Rectangle | `<rect width="80" height="40" />`                          |
| 3.  | Circle    | `<circle cx="50%" cy="50%" r="60" />`                      |
| 4.  | Ellipse   | `<ellipse cx="100" cy="50" rx="80" ry="40" />`             |
| 5.  | Polygon   | `<polygon points="100,10 40,198 190,78 10,78 160,198" />`  |
| 6.  | Polyline  | `<polyline points="100,10 40,198 190,78 10,78 160,198" />` |

---

# Topics for you to explore more

- More complex SVG elements such as patterns, filters, paths
- Accessibility of SVGs
- Performance of SVGs

---

# More Resources

- [MDN Web Docs on SVG](https://developer.mozilla.org/en-US/docs/Web/SVG)
- [CSS Tricks - how to scale SVG](https://css-tricks.com/scale-svg/)
- [Smashing Magazine - SVG Generators](https://www.smashingmagazine.com/2021/03/svg-generators/)
- [Frontend Masters - SVG Essentials & Animations v2](https://frontendmasters.com/courses/svg-essentials-animation/?utm_source=css-tricks&utm_medium=website&utm_campaign=css-tricks-tags-sidebar)

---

# Thank you!

Hope you enjoyed the L&L 😄 

Any questions? 

--

[Feedback form](https://forms.gle/HQ8JoEL3MuESbbVP9)

<img src="https://raw.githubusercontent.com/lyqht/intro-to-svg-slides/main/public/survey.svg" class='h-50' />
