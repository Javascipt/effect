# Effect

![Effect](https://travis-ci.org/Javascipt/effect.svg)

Effect is a node package that allows you to add effects on images.

## Table of contents:
- [Dependencies](#dependencies)
- [Installation](#installation)
- [How does it work](#how-does-it-work)
- [License](#license)

### Dependencies:

> This package depends on [the software ImageMagick], you need to get it [installed] before being able to use Effect package.

### Installation
```sh
$ npm install effect
```

### How does it work

After requiring the effect module :
```javascript
  var effect = require('effect');
```
you can use the following method (effects):
 - blur
 - gaussian
 - sharpen
 - unsharp
 - threshold
 - oilpaint
 - sketch
 - metal
 - edge
 

Every method's name gives an idea on the effect that will be applied on the specified image.
The arguments of all the methods are the same, let's take the method `blur` as example:

```Javascript
 var options = {
    image : './path/to/your/image.jpg',
    to : './path/to/target.jpg', /* optional, if not specified, the main image will be overwritten */
    level : 5, /* optional, level of the effect that will be applied (default value : 5) */
    size : 200, /* optional, you can resize your image while applying the effect (default value : 100%) */
 };
 
 var callback = function (error) {
    if(!error) {
        console.log("The effect was applied to your image !");
    }
 }
 
 effetc.blur(options, callback);
```

## License
MIT

   [the software ImageMagick]: <http://www.imagemagick.org/>
   [installed]: <http://www.imagemagick.org/script/binary-releases.php/>
