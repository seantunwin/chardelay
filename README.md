# Chardelay.js

A stand-alone library for placing content on the page with a delay similar to a typing effect.

Compatible with most modern browsers, including IE8+.

## Project Setup

Download and unzip or clone then copy `chardeley.min.js` into your project's js folder.

Since this is stand-alone there are no dependencies, although it is ready to accept a jQuery element object.

## How to use

### Add the javascript file to your page:

```html
<script src="js/chardelay.min.js"></script>
```

### Create a new instance

_Able to initialize in a few ways_:

`var myChardelay = Chardelay( contentString );` -- Uses `defaults` for `options`.

`var myChardelay = Chardelay( contentString, "container", "h", 300, "p", "coolText", false );`

```js
var myChardelay = Chardelay( contentString, {
                      "parentEl": $("#container"),
                      /* OR if not using jQuery:
                       * "parentEl": document.getElementById("container")
                       * "parentEl": document.querySelector(".myClass")
                       */
                      "layout"  : "v",
                      "delay"   : 225,
                      "inEl"    : "div",
                      "css"     : "shadow",
                       "multi"  : true

                  });
```

#### _Arguments:_

1. `content`: String, Number, or Array of that which is to be outputted. _Required_.
2. Options:
    1. `parentEl`: Object of parent element for `inEl` to be used as a container. Must be a valid HTML element object. Accepts element by Id, Class, or jQuery element object. _Default_: `document.body`.
    2. `layout`: String of output display - `"h"` = horizontal, `"v"` = vertical. _Default_: `"h"`.
<<<<<<< HEAD
    3. `delay`: Number of milliseconds between placing output items. Must be greater than 0 or default will be used. _Default_: `150`.
=======
    3. `delay`: Number of milliseconds between placing output items.  Must be greater than 0 or default will be used. _Default_: `150`.
>>>>>>> b89422811066bf6923a05a3aef724e1e06f8b2a4
    4. `inEl`: String of type of HTML element to create for our output to be placed inside. Accepted types are `"p"`, `"span"`, `"div"`. _Default_: `span`. 
    5. `css`: String of CSS class for output to be styled as. Note: No dot(.). _Default_: `chardelay`.
    6. `multi`: Boolean to stipulate whether the content is to be placed inside a single HTML element or each item of content gets it's own element. _Default_: `false`.


## Troubleshooting

* If there is more than 1 element in the returned `NodeList` for `parentEl` only the first element will be used.

## License

Copyright (c) 2013 [@seantunwin](https://twitter.com/seantunwin) Licensed under the MIT license.
