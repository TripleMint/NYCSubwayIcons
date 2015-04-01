# NYCSubwayIcons

CSS Subway Icons for the Subway Lines in NYC
http://www.mta.info/developers/resources/line_colors.htm


## EXAMPLE / USAGE

    <element class="subway-icon subway-circle-1">
        <element class="subway-text">1</element>
    </element>

I would suggest using spans for simplicity.

.subway-icon is only a suggestion since you will probably want a different size
depending on viewport. For example:

```CSS
.subway-icon {
    // text size times 1.3 (2*1.3)
    height: 2.6em;
    width: 2.6em;
}
.subway-text {
    font-size: 2em;
}
```

if you are implementing this using SASS (.sass) you can just use the mixins
directly especially to get the right height/width comparative to the font
size. For example:

```SASS
$size: 2em
.subway-icon
    +subway-circle-size($size)
.subway-text
    font-size: $size
```

If for some reason the 1.3 ratio doesnt look right to you you are obviously
free to augment the relation between these sizes as you see fit, this has
simply seemed to work well for us given our ems. In practice we have noticed
that smaller sizes the ratio seems to fall apart and we recommend setting
values for width, height and font-size that work manually.

That way you don't need to reapply the mixin after media query, which keeps your CSS
way smaller. This is a good general rule to keep in mind, isolate the things that change
from the things that don't.

Obviously you can choose any naming conventions you want, the key is to have the colors
and the mixins

## TODO
 * Add some actual implementation examples
 * github.io project page.

## Contributing
Process the sass however you see fit. We like to provide it both minified and non minified for easier reading. This is just a suggestion if you have the SASS gem installed.

### Basics

 * Forkit
 * Edit it
 * Submit a Pull Request

### Compiling SASS

Edit the sass file, not the CSS files. To learn more about the SASS language go [here](http://sass-lang.com/).

    $ sass --style expanded NYCSubwayIcons.sass NYCSubwayIcons.css
    $ sass --style compressed NYCSubwayIcons.sass NYCSubwayIcons.min.css


### Authors
Chris DiLorenzo, Chris Sanders & Ethan Schmertzler

### License stuff
Copyright (c) 2015 Suitey

License: The MIT License (MIT)

http://www.opensource.org/licenses/mit-license.php
