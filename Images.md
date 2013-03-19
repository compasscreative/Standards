Images
======

- Please be conscious of your image formats. Images tend to account for the largest amount of bandwidth on a website.
- We tend to save `JPG` images at `80-90%` compression in Photoshop.
- Use `PNG` files where needed. [ImageAlpha](http://pngmini.com/) is an excellent program for reducing PNG file sizes while still maintaining a full alpha channel.
- Consider using `SVG` (vector) files, with fallbacks for non supporting browsers. SVG images look great on retina displays. Use [Modernizr](http://modernizr.com/) to check for SVG support.
- In general, try to reduce the amount of images loaded. Where possible, merge multiple images into CSS sprites.
- Do not use JavaScript for image rollovers, instead use CSS sprites.
- Where possible, do not use images for text. With the availability of fonts using Font-face this can often be avoided.
- Please include a site icon (`favicon.ico`), as well as all the standard Apple touch icons. Please see the [HTML5 Boilerplate](https://github.com/h5bp/html5-boilerplate) for a complete list.