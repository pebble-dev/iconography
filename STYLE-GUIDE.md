# Style Guide

### Pebble icons use a **limited set of angles.**
![](./github-images/angle%20limits.png)

Shallow angles and misaligned pixels lead to a fuzzy, uneven look when drawn on a real watch. Ensure your lines render well at very low resolution, with and without anti-aliasing.

Rebble designers have hand-picked the angles 1:1 (45°), 2:1 (26.57°), and 3:1 (18.43°) for their even, consistent stair-stepping on every watch. Check how your icon rasterizes, in [pdc_tool](https://pdc-tool.heikobehrens.com/) or on a real watch.

### Ensure strokes are aligned with the pixel grid
![](./github-images/pixel%20alignment.png)

Ensure that your points snap to pixels and half-pixels for PDC compatibility. Strokes of even width should fall on a grid line, and strokes of odd width should start in the center of a pixel, in order for the edge of a stroke to fill an entire pixel.

### Notification and Timeline icons come in three sizes: **25x25, 50x50,** and **80x80**.
![](./github-images/Three%20sizes.png)
 
- At 25px, solid lines are **2px thick**.
- At 50px, solid outlines are **3px thick**, but you can use thinner lines for detail.  
(Tip: When designing for 3px lines, have your points snap to the center of the pixel. This ensures the line edges fall between the pixels.)
- At 80px, solid outlines are **4px thick**, but you can use thinner lines for detail.

### Pebble icons use **closed shapes** with **filled backgrounds**.
![](./github-images/closed%20shapes%20solid%20fill.png)

Pebble illustrations do use open lines, for motion or for secondary elements, but an icon always contains a focal area with a solid white fill.

## Tools
-  [**pdc_tool CLI**](https://github.com/HBehrens/pdc_tool) - @HBehrens has made a wonderful command-line tool for working with Pebble graphics, capable of converting between SVG and PDC formats and producing pixel-perfect renders.
- [**pdc_tool Web Version**](https://pdc-tool.heikobehrens.com/) - @HBehrens has also developed a web-based version of pdc_tool. It takes standard SVG vector graphics or existing PDC files and renders them in your browser — pixel-perfectly, just like on a real Pebble watch.
- [**pdc_tool Inkskape Plugin**](https://github.com/hellcp/inkscape-pdc-exporter) - @hellcp has created a plugin for Inkscape that integrates `pdc_tool` for easy export and live preview.

## Technical details
**[Pebble Draw Commands](https://developer.rebble.io/developer.pebble.com/docs/c/Graphics/Draw_Commands/index.html)** are a set of vector graphics routines on Pebble smartwatches, intended to display and animate graphics using less memory and storage than bitmaps. They can encode open or closed paths, as well as circles, and contain information about stroke width, stroke color, and optional fill color. For an introduction to using PDC graphics in Pebble apps, read the guide [here](https://developer.rebble.io/guides/graphics-and-animations/vector-graphics/index.html).

Read more about the subset of compatible SVG elements [here](https://developer.rebble.io/guides/app-resources/converting-svg-to-pdc/index.html)

## Submission guidelines
Create a PR to this repo with your SVGs in the appropriate folders, following the naming structure `<size>px_Name_of_icon.svg`

Please also add your icons to the gallery in the [README.md](./README.md) file.

## Recommended Reading
A holistic understanding of designing for Pebble's limitations is great to have.
- [Designing Apps for Pebble | Pebble Developer Retreat 2015](https://www.youtube.com/watch?v=LuiK8ZiPXr4) (YouTube Video)
- [Core Experience Design - Rebble Developer Website](https://developer.rebble.io/guides/design-and-interaction/core-experience/index.html)
- [Storytelling in Pixels](https://web.archive.org/web/20250323041252/https://old.heydays.no/project/pebble/) (via Internet Archive Wayback Machine)
