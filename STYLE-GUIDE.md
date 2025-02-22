# Style Guide

### Pebble icons use a **limited set of angles.**
![](./github-images/angle%20limits.png)

Shallow angles and misaligned pixels lead to a fuzzy, uneven look when drawn on a real watch. Ensure your lines render well at very low resolution, with and without anti-aliasing.

Rebble designers have hand-picked the angles 1:1 (45°), 2:1 (26.57°), and 3:1 (18.43°) for their even, consistent stair-stepping on every watch. Check how your icon rasterizes, in [pdc_tool](https://github.com/HBehrens/pdc_tool) or on a real watch.

### Notification and Timeline icons come in three sizes: **25x25, 50x50,** and **80x80**.
![](./github-images/Three%20sizes.png)
 
- At 25px, solid lines are **2px thick**.
- At 50px, solid outlines are **3px thick**, but you can use thinner lines for detail.
- At 80px, solid outlines are **4px thick**, but you can use thinner lines for detail.

### Pebble icons usually use **closed shapes** with **filled backgrounds**.
![](./github-images/small%20icons%20preview.png)

## Tools
- @HBehrens has made a wonderful command-line tool for working with Pebble graphics, capable of converting between SVG and PDC formats and producing pixel-perfect renders: https://github.com/HBehrens/pdc_tool
- @hellcp has a plugin for Inkscape that integrates `pdc_tool` for easy export and live preview: https://github.com/hellcp/inkscape-pdc-exporter
- ...

## Technical details
**[Pebble Draw Commands](https://developer.rebble.io/developer.pebble.com/docs/c/Graphics/Draw_Commands/index.html)** are a set of vector graphics routines on Pebble smartwatches, intended to display and animate graphics using less memory and storage than bitmaps. They can encode open or closed paths, as well as circles, and contain information about stroke width, stroke color, and optional fill color. For an introduction to using PDC graphics in Pebble apps, read the guide at https://developer.rebble.io/developer.pebble.com/guides/graphics-and-animations/vector-graphics/index.html

Read more about the subset of compatible SVG elements at https://developer.rebble.io/developer.pebble.com/guides/app-resources/converting-svg-to-pdc/index.html

## Submission guidelines
Create a PR to this repo with your SVGs in the appropriate folders, following the naming structure `[Name] [size]px.svg`

## Recommended Reading
A holistic understanding of designing for Pebble's limitations is great to have.
- https://www.youtube.com/watch?v=LuiK8ZiPXr4
- https://developer.rebble.io/developer.pebble.com/guides/design-and-interaction/core-experience/index.html
- https://old.heydays.no/project/pebble/
