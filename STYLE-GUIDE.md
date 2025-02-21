# Style Guide

### Pebble icons use a **limited set of angles.**
![](./github-images/angle%20limits.png)

Shallow angles and misaligned pixels lead to a fuzzy, uneven look when drawn on a real watch. Ensure your lines render well at very low resolution, with and without anti-aliasing.

Rebble designers have hand-picked the angles 1:1 (45°), 2:1 (26.57°), and 3:1 (18.43°) for their even, consistent stair-stepping on every watch. Check how your icon rasterizes, in https://github.com/HBehrens/pdc_tool or on a real watch.

### Notification and Timeline icons come in three sizes: **25x25, 50x50,** and **80x80**.
![](./github-images/Three%20sizes.png)
 
- At 25px, solid lines are **2px thick**.
- At 50px, solid outlines are **3px thick**, but you can use thinner lines for detail.
- At 80px, solid outlines are **4px thick**, but you can use thinner lines for detail.

### Pebble icons usually use **closed shapes** with **filled backgrounds**.
![](./github-images/small%20icons%20preview.png)

## Technical details
@HBehrens has made a wonderful command-line tool for working with Pebble vector graphics files and SVGs: https://github.com/HBehrens/pdc_tool

Read the limitations on SVG compatibility at https://developer.rebble.io/developer.pebble.com/guides/app-resources/converting-svg-to-pdc/index.html

...

## Submission guidelines
Create a PR to this repo with your SVGs in the appropriate folders, following the naming structure `[Name] [size]px.svg`

## Recommended Reading
A holistic understanding of designing for Pebble's limitations is great to have.
- https://www.youtube.com/watch?v=LuiK8ZiPXr4
- https://developer.rebble.io/developer.pebble.com/guides/design-and-interaction/core-experience/index.html
- https://old.heydays.no/project/pebble/
