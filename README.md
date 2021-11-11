![](./intro-to-svg-slides-cover.png)

This repository contains slides accompanying an internal lunch & learn session in Thoughtworks on Intro to SVG, that happened on 12 November 2021.

Slides are built with [Slidev](https://github.com/slidevjs/slidev), with the [Penguin](https://github.com/alvarosaburido/slidev-theme-penguin) theme which I have slightly modified.

---

# SVG Element Basics Cheatsheet


| Shape     | Usage Example                                                                                                | Result                                                                                                                                                   |
| --------- | ------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Square    | `<rect x="50%" y="50%" width="40" height="40" fill='#abcbca' />`                                             | <svg><rect x="50%" y="50%" width="40" height="40" fill='#abcbca' /></svg>                                                                                |
| Rectangle | `<rect x="50%" y="50%" width="80" height="40" fill='#abcbca' />`                                             | <svg><rect x="50%" y="50%" width="80" height="40" fill='#abcbca' /></svg>                                                                                |
| Circle    | `<circle cx="50%" cy="50%" r="60" fill="#abcbca" />`                                                         | <svg><circle cx="50%" cy="50%" r="60" fill="#abcbca"  /></svg>                                                                                           |
| Ellipse   | `<ellipse cx="100" cy="50" rx="80" ry="40" fill='#abcbca' />`                                                | <svg><ellipse cx="50%" cy="50%" rx="80" ry="40" fill='#abcbca' /></svg>                                                                                  |
| Polygon   | `<polygon points="100,10 40,198 190,78 10,78 160,198"  fill='#abcbca' stroke='#123123' stroke-width='5'  />` | <svg height='100' viewbox='0 0 300 300'><polygon points="100,10 40,198 190,78 10,78 160,198"  fill='#abcbca' stroke='#123123' stroke-width='5'  /></svg> |
| Polyline  | `<polyline points="100,10 40,198 190,78 10,78 160,198" fill='#abcbca' stroke='#123123' stroke-width='5' />`  | <svg height='100' viewbox='0 0 300 300'><polyline points="100,10 40,198 190,78 10,78 160,198" fill='#abcbca' stroke='#123123' stroke-width='5' /></svg>  |