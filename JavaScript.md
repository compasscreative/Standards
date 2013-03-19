JavaScript
==========

- All JavaScript files should be concatenated into one file and minified, and included in the footer of the website, right above the `</body>` tag. Again, [Codekit](http://incident57.com/codekit/) is an excellent tool that can help here.
- The only exception to this rule is for [Modernizr](http://modernizr.com/), which must be placed inside the  `<header>` tag.
- If using a JavaScript library, [jQuery](http://jquery.com/) is preferred. jQuery plugins we typically use are:
    - [jQuery.Fancybox](http://fancyapps.com/fancybox/)
    - [jQuery.Cycle](http://jquery.malsup.com/cycle/)
    - [jQuery.Validation](http://bassistance.de/jquery-plugins/jquery-plugin-validation/)
    - [jQuery.Form](http://www.malsup.com/jquery/form/)
- **Please do not** use any in-line JavaScript, other than Google Analytics (which should be the very last item on the page).
- We will provide a Google Analytics code. Please ask us if you did not receive this on your project.