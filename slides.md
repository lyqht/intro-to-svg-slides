---
# try also 'default' to start simple
theme: penguin
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: prism
# show line numbers in code blocks
lineNumbers: true
# some information about the slides, markdown enabled
info: |
  ## Slides for Intro to SVG L&L
# persist drawings in exports and build
drawings:
  persist: false
layout: intro
---

# Intro to SVG


<div class="pt-12" v-click>
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Let's start <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
layout: presenter
presenterImage: 'https://pbs.twimg.com/profile_images/1441783883456942080/vV37mSqv_400x400.jpg'
---

# Estee Tey

Software Developer at <fancy-link  href="https://www.thoughtworks.com/" favicon="https://www.google.com/s2/favicons?domain=thoughtworks.com" >Thoughtworks</fancy-link>

- I have a tech blog at <fancy-link href="https://esteetey.dev">esteetey.dev</fancy-link>
- Connect with me at <fancy-link href="https://twitter.com/estee_tey">@estee_tey</fancy-link>

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

# Images

![raster vs vector images](https://vector-conversions.com/images/vector_vs_raster.jpg)

<!-- Images comprise up to 60%-65% of bytes on most web pages and page size is a major factor in total rendering time. Page size is especially important for mobile devices, where smaller size images will help to save both bandwidth and battery life. -->

---

# Image File Types

| File Extension                          | Description                                                      |
| --------------------------------------- | ---------------------------------------------------------------- |
| <code>.png</code>                       | Portable Network Graphic                                         |
| <code>.jpg</code>  / <code>.jpeg</code> | Image format by Joint Photographic Experts Group                 |
| <code>.webp</code>                      | A superior image format of <code>.png</code> & <code>.jpg</code> |
| <code>.gif</code>                       | Graphics Interchange Format                                      |
| <code>.svg</code>                       | Scalable Vector Graphics                                         |

---

# How to get SVG

1. Extract from websites
2. Generate SVG
3. Create SVG from scratch

---
layout: center
class: text-center
---
# Extract from websites

[SVGOMG](https://jakearchibald.github.io/svgomg/) Demo with Hacktoberfest's SVG

---

# Generic Shapes for SVG



<Tweet id="1455232312770273281" />
---

# Generate SVG


---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

# Create SVG with code

```html
<svg 
  version="1.1"
  baseProfile="full"
  width="300" height="200"
  xmlns="http://www.w3.org/2000/svg">
  <rect width="100%" height="100%" fill="black" />
</svg>
```

<arrow v-click="3" x1="400" y1="420" x2="230" y2="330" color="#564" width="3" arrowSize="1" />
