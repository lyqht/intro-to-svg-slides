This article is an enhanced version of the lunch & learn session that I presented recently on **Introduction to Scalable Vector Graphics.**


%%[svg-slides]

The slides can be found [here](https://lyqht.github.io/intro-to-svg-slides), where you can choose to download a PDF version.

---

# What is SVG?

SVG refers to **S**calable **V**ector **G**raphics, and it is a type of image format that is widely available on websites. Before we describe further on SVG, let's understand the importance of images and other image format types.

### 🖼 Images

On a very high level, we can split images into 2 generic types: **Raster** and **Vector**.

Raster images are drawn pixel by pixel, and may look different depending on the *resolution/ pixel density* of the device. Vector images look good and crisp *regardless of the resolution*. Here's a Codepen to illustrate the difference between the two, try **resizing** the different images! ✨

%[https://codepen.io/lyqht/pen/RwZeZNm]

The raster art was drawn by my boyfriend using Microsoft Paint (what a madlad! 😍), while the vectorized version are traced and coloured by me using Adobe Illustrator. It was a joint project for creating a couple tee design 😉 The resizable functionality is provided by [Interact.js](https://interactjs.io/docs/resizable/).

If vector images always look good, then why would we ever consider raster images? Well that's because of 2 practical factors. The first being the fact that the technology to support the *creation* & *usage* of raster images is much more accessible compared to SVG. 

- On the designers' side, there is generally more familiarity to work with tools to create raster art (Photoshop) than vector art (Illustrator).
- On the developer's side, most file uploaders e.g. for uploading avatar images, background banners etc, are implemented to be restricted to raster image formats only.

The second reason for preferring raster images over SVG is the **file size**. Different image formats of the same visual will result in different file sizes, and thus different pages sizes. According to *[Google Developers Page on Image Compression](https://developers.google.com/speed/webp/docs/compression),*

> *Images comprise up to 60%-65% of bytes on most web pages and page size is a major factor in total rendering time. Page size is especially important for mobile devices, where smaller size images will help to save both bandwidth and battery life.*

For **different use cases,** we should be using different image file types. In the context of online images, 

- For Raster Image File Types, there's 4 types - GIF, PNG, JPG and WEBP.
- For Vector Image File Types, there's only SVG!

Here's a table for the description of the name of the file extensions.

![Table showing file extensions](https://cdn.hashnode.com/res/hashnode/image/upload/v1637037579358/aSzqOFyrq.jpeg)
And here's a brief context behind how each raster file type came about.

1. GIF
    - GIF was **one of the first two graphics formats supported** by HTML, along with [XBM](https://en.wikipedia.org/wiki/X_BitMap).
2. PNG ****
    - PNG was cretated to improve upon and **replace GIF** (Graphics Interchange Format) as an image-file format.
    - It supports a better compression algorithm and also transparency in an image.
3. JPG
    - The original file extension for the Joint Photographic Expert Group File Format was `.jpeg`. On Mac, this was supported but on Windows, all files required a **3-letter file extension**. So, the file extension was shortened to `.jpg`.
    - Eventually, with upgrades Windows also began to accept `.jpeg`. However, many users were already used to ‘.jpg’, so both the 3-letter file extension and the 4-letter were commonly used, and still are.
    - Today, the most commonly accepted and used form is the `.jpg`, as **many users were Windows users**.
4. WEBP
    1. WEBP is an image format type developed by Google to create files that are smaller for the same quality of JPEG, PNG, and GIF image formats.

Now that we know what image formats are commonly used for web images, now we can talk about why we should use SVG.
---

Here's a table to illustrate the colour modes, compression and the intended usage for different image file types.


![Intro to SVG_Page_14.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1637037980630/hNf4rc5cx.jpeg)

## Why use SVG?

1. SVG is **scalable**
    1. You can stretch it however much, you still won't lose quality because of resolution issues.
    2. Responsive design is easier to be achieved!
2. SVG can be coded **inline** 
    - this reduces the HTTP requests required to retrieve media.
    - this also meant that the FOUC (Flash of Unstyled Content) problem is less likely to happen from media not being retrieved and styled before rendering in the page.
3. Developers can work with the individual nodes in the SVG to:
    1. animate
    2. optimize for performance
    3. optimize for accessibility
    
    > Animation and optimization are considered a little more advanced so they are not covered in this introductory article. Do watch out for my future articles for these 😊

# How to create SVG?

In this article, I will show you 2 different ways of creating SVG. The first would be using code to create SVG XML and the other would be to use Figma, a design tool to create SVG.

## Create SVG with Code

For learning to create SVG with code, we will **create 4 simple country flags from SEA** (Southeast Asia) - *Japan, Thailand, Vietnam and Singapore*. With these 4 flags, we will learn 4 basic elements. 

<div>
    <img src="">
</div>

### ⛳ 1st Flag: Japan

![Slide on JP Flag](https://cdn.hashnode.com/res/hashnode/image/upload/v1637041966658/lopW84pcW.jpeg)

The flag has 2 colors and 2 shapes. The color of SVG elements are indicated by the `fill` property. The shapes are created by the following HTML tags.

- `<rect />`
- `<circle />`

For the rectangle, the width and height properties are pretty self-explanatory. 

For the circle, 

- `(cx, cy)` are x,y coordinates of the centre point of the circle
- `r` represents the radius of the circle
- Hence to make the circle positioned in the center, we set `(cx, cy)` to be both a *relative* 50%. If you prefer *absolute units*, you could set the rect's width=300 and circle's cx=150 instead.

```html
<svg>
    <rect width="100%" height="100%" fill="white" />
    <circle cx="50%" cy="50%" r=60 fill="#BC002D" />
</svg>
```

<img src="https://raw.githubusercontent.com/lyqht/intro-to-svg-slides/main/public/svg/flags/JP.svg" />

---

## ⛳ 2nd Flag: Thailand

![Slide on TH Flag](https://cdn.hashnode.com/res/hashnode/image/upload/v1637038738073/LYxYYiPAP.jpeg)

This simple example has only 5 rectangles, and is meant to introduce you to **positioning**. Previously we have the circle centered in the middle of the rectangle by setting the `(cx, cy)` coordinates. For other elements, usually you can set the `(x, y)` coordinates directly. These `(x, y)` coordinates always refer to the **top left coordinate** of the element

```html
<svg>
    <rect width="100%" height="20%" y="0" fill="red" />
    <rect width="100%" height="20%" y="20%" fill="white" />
    <rect width="100%" height="20%" y="40%" fill="blue" />
    <rect width="100%" height="20%" y="60%" fill="white" />
    <rect width="100%" height="20%" y="80%" fill="red" />
</svg>
```

<img src="https://raw.githubusercontent.com/lyqht/intro-to-svg-slides/main/public/svg/flags/TH.svg" />

---

### ⛳ 3rd Flag: Vietname

![Slide on VN Flag](https://cdn.hashnode.com/res/hashnode/image/upload/v1637038742204/QUUv0b2aQ.jpeg)

There are 2 shapes here - a rectangle and a star. There isn't a `<star />` element unfortunately, but there is a generic `<polygon />` element that we can use to create a star. W3C provides [many examples of shapes](https://www.w3schools.com/graphics/svg_examples.asp), so I will take their star example and use it here.

Example of creating a star with the polygon element

```html
<svg>
	<polygon id="star" fill="yellow"
      points="100,10 40,198 190,78 10,78 160,198" />
</svg>
```

However, if we try to preview the svg with this star, it will get cut off. 

<img src="https://raw.githubusercontent.com/lyqht/intro-to-svg-slides/main/public/svg/shapes/star-cutoff.png" />


This is because the star is bigger than the SVG's **default width & height** of **300×150**. 

To fix this, we could adjust the coordinates one by one but that's painful so let's not do that 😅. Instead, let's change the `viewbox` property. 

> ⚠ The `viewbox` property is the most important thing you have to know about SVG.
> 

The `viewbox` can be declared by giving it a min-x, min-y, width and height. For us to see the star entirely, the height needs to ≥198, since the *biggest y-coordinate* we have in the SVG is 198. Let's also give the star a little padding, so we will increase both the width and height of the SVG viewbox.

```html
<svg viewbox='0 0 300 300'>
    <polygon id="star" fill="yellow" points="100,10 40,198 190,78 10,78 160,198" />
</svg>
```

Now we can see the star

<img src="https://raw.githubusercontent.com/lyqht/intro-to-svg-slides/main/public/svg/shapes/star.png" />

> For a more in-depth explanation on scaling SVG, you can refer to this nifty [article by CSS-Tricks](https://css-tricks.com/scale-svg/). 

Let's move on to create the actual VN flag.

In the flag, the star actually looks a lot smaller than what we have created just now with the padding. We can modify the `viewbox` of this star so that it looks smaller, but at the same time, we want the flag to still look like its original shape of a small rectangle that follows the default `viewbox` of 300x150.

There're different ways of to implement the flag, but here, I will introduce you to a new concept - **Nesting of SVG elements.** We can enclose the SVG element for the star within another SVG element tag. That way, we can achieve the scaling down of the star element while keeping the flag's size. We will also add some `(x, y)` offsets so that the star looks centered.

```jsx
<svg>
  <rect width="100%" height="100%" fill="red" />
  <svg viewBox="100 0 600 600" x="25%" y="25%">
    <polygon id="star" fill="yellow"
      points="100,10 40,198 190,78 10,78 160,198" />
  </svg>
</svg>
```

<img src="https://raw.githubusercontent.com/lyqht/intro-to-svg-slides/main/public/svg/flags/TH.svg" />

---

Now that you understand how the `<polygon />` element works, you can also learn about the `<polyline />` element.

![Intro to SVG_Page_21.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d9eb5c4a-f440-4b61-bfdf-10d92e631fa4/Intro_to_SVG_Page_21.jpg)

The only difference polygon and polyline is that the polygon is a **closed path** while the polyline is an **open path** - that's why if you draw the 2 shapes in SVG and give them stroke colors, you can tell the difference. 

- In `<polyline />`, the last point is not connected to the first point
- In `<polygon />`, the last point is connected to the first point

---

### ⛳ 4th Flag: SG

For the 4th country flag, we are creating my home nation, Singapore! 😊

![Slide on SG Flag](https://cdn.hashnode.com/res/hashnode/image/upload/v1637038744584/pOqTH2pCO.jpeg)

The flag comprises of 2 rectangles, 5 stars and 1 moon. To create this flag, it requires the combination of concepts that we have learnt from the previous flags.

But how do we draw a moon? Well, when it comes to art, we don't always have to follow the semantic way of creating things. We can just create 2 overlapping circles where the top circle is red and the bottom circle is white, so that the result looks like a moon 🌘

Since we have already created a star before, let's reuse it and just change the fill to white. To reuse an element, we can declare **definitions** in a `<defs>` tag and **use** them using a `<use>` tag. You can see that this becomes helpful as we reuse the same element multiple times.

```html
<svg>
		<defs>
		    <polygon 
					id="white-star" 
					points="100,10 40,198 190,78 10,78 160,198" 
					fill="white" />
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
```

<img src="https://raw.githubusercontent.com/lyqht/intro-to-svg-slides/main/public/svg/flags/SG.svg" />


---

🎉 Good job reaching here thus far!

🥳 We managed to create SVGs of **4 different SEA country flags using code!**

👉 You can find all the `.svg` files covered [here](https://github.com/lyqht/intro-to-svg-slides/tree/main/public/svg/flags).

For the rest of the article, I promise you the content would be much *lighter*! 😊 Now, let's move on to creating SVG graphics using **Design Tools**.

---

## 🎨 Create SVG with Design Tools

Common Design Tools used to create SVG include

1. <a href="https://www.figma.com"><img width=40 src="https://cdn.freebiesupply.com/logos/thumbs/2x/figma-1-logo.png" /> Figma</a> 
2. <a href="https://www.sketch.com/"><img width=40 src="https://cdn.iconscout.com/icon/free/png-256/sketch-61-722739.png" /> Sketch</a> 
3. <a href="https://www.adobe.com/sg/products/illustrator.html"><img width=40 src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fb/Adobe_Illustrator_CC_icon.svg/1200px-Adobe_Illustrator_CC_icon.svg.png" /> Illustrator</a> 

Out of the 3 options, Figma is free and also accessible on any platform, so I will share with you a very short intro on Figma on creating graphics using **Paths,** and **exporting them as SVG**.

%%[intro-to-svg-figma]

👉 **Access the Figma demo file [here](https://www.figma.com/file/vHcMllyWIi5lPMhKldSI7k/intro-to-svg-shapes?node-id=0%3A1).** 

> Feel free to inspect anything! If you like, you can also create a duplicate of the file so that you can try playing around with the Paths (requires login to Figma).
> 
> ⭐ Pro tip: To edit any path, click on a path and press the 'Enter' key.

### Straight Paths

Using the **Pen Tool (P key) 🖊**, you can easily create straight paths and form polygons, polylines and shapes like the low-poly bear!

![Figma-Pentool-demo.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1637042456734/PPAXvKG_S.gif)


### Curved Paths

After creating straight paths with the Pen Tool, you can use the **Bend Tool (Ctrl Key)** to create a **Bezier Curve**. 

![Bezier Curve Handles On Figma](https://cdn.hashnode.com/res/hashnode/image/upload/v1637042292395/-Lg_hGg97.png)

Handles will appear, connected to the start and end coordinate of the path that you have selected. This is how shapes like the bunny's round head & ears are created!

![Figma-BendTool-demo.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1637042606762/HtxhCtyTq.gif)



Another type of curved Path would be the **Arc**. After creating an Ellipse, you can hover over the ellipse path to use the **Arc Tool** to create an Arc. 

![Figma_Arc_Demo.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1637042177526/XmtlqpiaA.gif)

### Exporting the SVG

Once you're done creating your fancy shapes and graphics, you can choose to export them easily as a SVG file.

---

That sums up how you can create SVG from scratch either using Code or Design Tools! Personally I would recommend you to create graphics using Design Tools because having GUI makes it so much easier and you just have to export the graphic as SVG later on. However, the downside of it is that you have less control over the actual SVG element nodes inside your graphic - and this may be a problem if you try to do animation or optimization.

Next, we will move on to using online tools to generate SVG for us. This will be of great help to those of us who are less inclined in visual designing from scratch 😆

---

# Generate SVG

🔖 There's an [extensive list of SVG generators by Smashing Magazine](https://www.smashingmagazine.com/2021/03/svg-generators) that you can check out! 

During the talk, I have shown a demo for just two generators that were listed there because I found them relevant to what I've been reading recently.

- [Squicley](https://squircley.app/) → provides configuration for you to generate SVG squircles, a shape that is similar to rounded circles but not identical. Thought this was a pretty funny concept of shape to introduce to you all 😄 Apparently, [this is what makes Apple hardware more distinct than others](https://99percentinvisible.org/article/circling-square-designing-squircles-instead-rounded-rectangles/).
    
    ![https://99percentinvisible.org/app/uploads/2017/10/not-apple-728x347.png](https://99percentinvisible.org/app/uploads/2017/10/not-apple-728x347.png)
    
- [SVGBackgrounds](http://SVGBackgrounds.com) → provides you many SVG backgrounds you can customize to be used for your next project. I also previously made a Tweet thread on how you can use it and why you should use it.

%[https://twitter.com/estee_tey/status/1444814549341782018]

Aside from generating SVG, we can also extract SVG that we see on websites using the Inspector ✨

---

### Extract SVG from websites

> ⚠️ **Important Note**: Please check if you can use the extracted SVG without attribution.
> 

For extracting SVG from websites, we will use our good old [Element Inspector](https://esteetey.dev/navigate-the-frontend-easily-with-the-inspector) to do it! Let's try it out on [Hacktoberfest's website](https://hacktoberfest.digitalocean.com/) since they have really beautiful flowers this year 🌺

1. Ctrl+F `"<svg>"` to find the SVG element that you want. 
2. Once the highlighted area matches the SVG that you're targeting, right click the element and choose "Copy Element"
3. The result will be something like this, which you can paste in a new `.svg` file.

![](https://raw.githubusercontent.com/lyqht/intro-to-svg-slides/main/public/svg/hacktoberfest.svg)

---

## 🌟 Bonus Helpful Tools for SVG

- Optimization of SVG file size: [SVGOMG](https://jakearchibald.github.io/svgomg/)
    - If you use design tools to create SVG or extract SVG from websites, chances are that most of them are not optimized in file sizes.
    - There's a handy tool called [SVGOMG](https://jakearchibald.github.io/svgomg/) which has many features you can toggle to help you optimize your file size, and you don't have to understand how all of them work.
    - You can also preview the result and the result file size at the circled area ✨
        
        ![Extract-SVG-From-Hacktoberfest-Website-Demo.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1637042863065/yHOCa9jBO.png)
        
- For React Devs: [Convert SVG to JSX](https://svg2jsx.com/)
    - You can paste SVG code here to be converted to either functional or class component syntax.

---

# FAQ

Q. I see `xmlns` attributes are used on SVG elements a lot, but you didn't use them in your talk at all, are they actually needed?

```
<svg xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/2000/svg"></svg>
```

A. TLDR: If you are using them as inline SVG, you don't need to include those. You only need those attributes if you are embedding them using the **img element**. Here's a useful [StackOverflow thread](https://stackoverflow.com/questions/18467982/are-svg-parameters-such-as-xmlns-and-version-needed) that answers this.

---

# That's a wrap folks! 🎉

Thank you for reading! If you have any questions or feedback for me, please leave them below, I'll attend to them shortly 😊 

If you find this article awesome, hit the reactions 🧡 and share it 🐦.

To stay updated whenever I post new stuff, follow me on [Twitter](https://twitter.com/estee_tey).