# Random Color

For generating attractive random colors. 

This is a PHP port of David Merfield [randomColor](https://github.com/davidmerfield/randomColor) Javascript utility.

See the results on [the demo](http://www.strangeplanet.fr/work/RandomColor.php).

[![Demo](http://llllll.li/randomColor/repo_demo.gif)](http://www.strangeplanet.fr/work/RandomColor.php)

### Options

You can pass an options object to influence the type of color it produces. The options object accepts the following properties:

**Hue** – Controls the hue of the generated color. You can pass a string representing a color name (e.g. 'orange'). Possible color names are *red, orange, yellow, green, blue, purple, pink and monochrome*.

**Luminosity** – Controls the luminosity of the generated color. You can pass a string containing *bright, light or dark*.

**Format** – A string which specifies the format of the generated color. Possible values are *hsv, hsl, hslCss, rgb, rgbCss, and hex*.

### Examples

```php

use \Colors\RandomColor;

// Returns a hex code for an attractive color
RandomColor::one(); 

// Returns an array of ten green colors
RandomColor::many(10, array(
   'hue' => 'green'
));

// Returns a hex code for a light blue
RandomColor::one(array(
   'luminosity' => 'light',
   'hue' => 'blue'
));

// Returns a hex code for a 'truly random' color
RandomColor::one(array(
   'luminosity' => 'random',
   'hue' => 'random'
));

// Returns a bright color in RGB
RandomColor::one(array(
   'luminosity' => 'bright',
   'format' => 'rgbCss' // e.g. 'rgb(225,200,20)'
));
```

### Other languages

RandomColor is available in [JavaScript](https://github.com/davidmerfield/randomColor), [c#](https://github.com/nathanpjones/randomColorSharped) and [go](https://github.com/hansrodtang/randomcolor).

### License

This project is licensed under the terms of the MIT license.
