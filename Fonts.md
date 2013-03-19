Fonts
=====

- For non-standard web fonts, please don't use Flash replacement or Cufón. Instead use the newer `@font-face` method.
- We will provide ready-to-go web fonts. Please ask us if you did not receive these on your project.
- [Bourbon](http://bourbon.io/) makes Font-face easy with their mixin:

        @include font-face('Font Name', '/fonts/font_file', bold);