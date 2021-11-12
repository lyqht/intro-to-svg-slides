![](./intro-to-svg-slides-cover.png)

This repository contains slides accompanying an internal lunch & learn session in Thoughtworks on Intro to SVG, that happened on 12 November 2021.

Slides are built with [Slidev](https://github.com/slidevjs/slidev), with the [Penguin](https://github.com/alvarosaburido/slidev-theme-penguin) theme which I have slightly modified.

---

# SVG Element Basics Cheatsheet

| Shape | Usage example | Result |
| :---         |     :---:      |          :---: |
| Square | `<rect x="50%" y="50%" width="40" height="40" fill='#abcbca' />` | ![image](https://user-images.githubusercontent.com/56090587/141361497-4f72efed-0524-4215-869b-96c7a8930b26.png) |
| Rectangle    | `<rect x="50%" y="50%" width="80" height="40" fill='#abcbca' />` | ![image](https://user-images.githubusercontent.com/56090587/141361970-1ed83c7b-777f-42dd-aca3-ee853efd25ba.png) |
| Circle    | `<circle cx="50%" cy="50%" r="60" fill='#abcbca' />` | ![image](https://user-images.githubusercontent.com/56090587/141362627-39d89b28-065b-4f5e-889d-49b57dfc970a.png) |
| Ellipse    | `<ellipse cx="100" cy="50" rx="80" ry="40" fill='#abcbca' />` | ![image](https://user-images.githubusercontent.com/56090587/141362910-9cbb8ef1-a98f-4c81-a80a-cedae147c049.png) |
| Polygon    | `<polygon points="100,10 40,198 190,78 10,78 160,198" fill='#abcbca' stroke="#123123" stroke-width="5" />` | ![image](https://user-images.githubusercontent.com/56090587/141363263-03dd9edc-2098-4f5f-9923-ff5d094f5605.png) |
| Polyline    | `<polyline points="100,10 40,198 190,78 10,78 160,198" fill='#abcbca' stroke="#123123" stroke-width="5" />` | ![image](https://user-images.githubusercontent.com/56090587/141363340-d51faf87-3e8d-4060-bf75-ed6387fc2d39.png) |

Special thanks to [Matej Bošnjak](https://github.com/mbos2) who helped to create the image results from the code.

<!-- 

| Shape     | Usage Example                                                                                                | Result                                                                                                                                                   |
| --------- | ------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Square    | `<rect x="50%" y="50%" width="40" height="40" fill='#abcbca' />`                                             | <svg><rect x="50%" y="50%" width="40" height="40" fill='#abcbca' /></svg>                                                                                |
| Rectangle | `<rect x="50%" y="50%" width="80" height="40" fill='#abcbca' />`                                             | <svg><rect x="50%" y="50%" width="80" height="40" fill='#abcbca' /></svg>                                                                                |
| Circle    | `<circle cx="50%" cy="50%" r="60" fill="#abcbca" />`                                                         | <svg><circle cx="50%" cy="50%" r="60" fill="#abcbca"  /></svg>                                                                                           |
| Ellipse   | `<ellipse cx="100" cy="50" rx="80" ry="40" fill='#abcbca' />`                                                | <svg><ellipse cx="50%" cy="50%" rx="80" ry="40" fill='#abcbca' /></svg>                                                                                  |
| Polygon   | `<polygon points="100,10 40,198 190,78 10,78 160,198"  fill='#abcbca' stroke='#123123' stroke-width='5'  />` | <svg height='100' viewbox='0 0 300 300'><polygon points="100,10 40,198 190,78 10,78 160,198"  fill='#abcbca' stroke='#123123' stroke-width='5'  /></svg> |
| Polyline  | `<polyline points="100,10 40,198 190,78 10,78 160,198" fill='#abcbca' stroke='#123123' stroke-width='5' />`  | <svg height='100' viewbox='0 0 300 300'><polyline points="100,10 40,198 190,78 10,78 160,198" fill='#abcbca' stroke='#123123' stroke-width='5' /></svg>  |

-->
