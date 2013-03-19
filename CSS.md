CSS
===

- We subscribe to the [progressive enhancement](http://en.wikipedia.org/wiki/Progressive_enhancement) web development philosophy. We understand that some items in our designs are not easily recreated in older browsers. This is okay! We'd prefer you use newer web technologies (ie. CSS3 features) than install polyfill or shims. If Internet Explorer 8 is missing the odd text shadow or border radius, no problem!
- If possible, please code CSS using the [SASS](http://sass-lang.com/) CSS preprocessing language. If you're not using a CSS preprocessor now, you'll thank us for recommending this.
- You're welcome to take it a step further, if you'd like, and use [Bourbon](http://bourbon.io/), a handy SASS mixin library.
- Include all SASS files under a folder named `/sass/` and keep the compiled CSS file in a folder named `/css/`.
- Please organize CSS rules similar to the following outline. Note, this style of coding will require [SASS](http://sass-lang.com/).

        .location (if necessary i.e. .footer or .blog_aside)
        {
            .module[_modifier]
            {
                .element
                {
                    // Position properties (sorted alphabetically)
                    clear: both;
                    position: relative;
                    top: 10px;

                    // Box properties (sorted alphabetically)
                    height: 500px;
                    margin: 0 10px 5px 2px;
                    padding: 5%;

                    // Decoration properties (sorted alphabetically)
                    background: #000;
                    color: black;
                    font-family: Arial;
                }
            }
        }

- All CSS stylesheets should be concatenated into one file for production use. This includes any vendor supplied CSS files. There are many different ways to do this, but we prefer [Codekit](http://incident57.com/codekit/). Codekit is a wonderful piece of software that will also compile your SASS to CSS.
- **Please do not** include any in-line CSS in your HTML markup.