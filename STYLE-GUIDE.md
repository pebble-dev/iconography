# Pebble Iconography Style Guide

### Pebble icons use a **limited set of angles.**
![](./github-images/angle%20limits.png)

Shallow angles and misaligned pixels lead to a fuzzy, uneven look when drawn on a real watch. Ensure your lines render well at very low resolution, with and without anti-aliasing.

Rebble designers have hand-picked the angles 1:1 (45°), 2:1 (26.57°), and 3:1 (18.43°) for their even, consistent stair-stepping on every watch. Check how your icon rasterizes, in [pdc_tool](https://pdc-tool.heikobehrens.com/) or on a real watch.

**Full list of permitted angles**:

- Horizontal (0°)
- 3:1 (18.43°)
- 2:1 (26.57°)
- 1:1 (45°)
- 1:2 (63.43°)
- 1:3 (71.57°)
- Vertical (90°)
- 1:3 (108.43°)
- 1:2 (116.57°)
- 1:1 (135°)
- 2:1 (153.43°)
- 3:1 (161.57°)
- Horizontal (180°) etc.

Make sure that every line angle uses a permitted ratio. This is easy to judge - for a 3:1 ratio, just remember that if you go along 3 pixels you need to go up/down 1 pixel, and every multiple of that. Or for the other quadrant, if you go up/down 3 pixels, then you must go along 1 pixel. Same rule for 2:1 and 1:1.

### Ensure strokes are aligned with the pixel grid
![](./github-images/pixel%20alignment.png)

- Ensure that your points snap to pixels and half-pixels for PDC compatibility. 
- Lines with strokes of 2px & 4px (even width) should fall on a grid line
- Lines with strokes of 3px (odd width) should start in the center of a pixel. This ensures that the edge of the stroke is always between two pixels.

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
- [**pdc_tool CLI**](https://github.com/HBehrens/pdc_tool) - @HBehrens has made a wonderful command-line tool for working with Pebble graphics, capable of converting between SVG and PDC formats and producing pixel-perfect renders.
- [**pdc_tool Web Version**](https://pdc-tool.heikobehrens.com/) - @HBehrens has also developed a web-based version of pdc_tool. It takes standard SVG vector graphics or existing PDC files and renders them in your browser — pixel-perfectly, just like on a real Pebble watch.
- [**pdc_tool Inkskape Plugin**](https://github.com/hellcp/inkscape-pdc-exporter) - @hellcp has created a plugin for Inkscape that integrates `pdc_tool` for easy export and live preview.

## Technical Details
**[Pebble Draw Commands](https://developer.rebble.io/developer.pebble.com/docs/c/Graphics/Draw_Commands/index.html)** are a set of vector graphics routines on Pebble smartwatches, intended to display and animate graphics using less memory and storage than bitmaps. They can encode open or closed paths, as well as circles, and contain information about stroke width, stroke color, and optional fill color. For an introduction to using PDC graphics in Pebble apps, read the guide [here](https://developer.rebble.io/guides/graphics-and-animations/vector-graphics/index.html).

Read more about the subset of compatible SVG elements [here](https://developer.rebble.io/guides/app-resources/converting-svg-to-pdc/index.html)

## Submission Guidelines

Before making a PR:

- Check your icons for errors. To test them, export each file to PDC in Inkscape using the [**pdc_tool Inkskape Plugin**](https://github.com/hellcp/inkscape-pdc-exporter). Fix any errors before proceeding - all lines must be straight, stroke widths must be integers, and points should snap to pixel or half pixel.
- Optimize each icon file. Remove embedded images, and save as "Optimized SVG" to reduce the filesize.
- Place SVGs in the appropriate folders, using the folder naming structure (e.g. `Name_of_icon_<size>px.svg`). No spaces in the filename - use underscores if needed.
- Add your icons to the gallery in [README.md](./README.md).
- Try to make a PR with a single commit - ideally squash any prior commits into one.

## Recommended Reading
A holistic understanding of designing for Pebble's limitations is great to have.
- [Designing Apps for Pebble | Pebble Developer Retreat 2015](https://www.youtube.com/watch?v=LuiK8ZiPXr4) (YouTube Video)
- [Core Experience Design - Rebble Developer Website](https://developer.rebble.io/guides/design-and-interaction/core-experience/index.html)
- [Storytelling in Pixels](https://web.archive.org/web/20250323041252/https://old.heydays.no/project/pebble/) (via Internet Archive Wayback Machine)
