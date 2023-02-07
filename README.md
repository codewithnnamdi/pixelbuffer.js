# Pixelbuffer.js
Pixelbuffer.js is a JavaScript library for manipulating pixel buffers. It is designed to be used in the browser, but can also be used in Node.js.

## Installation
Pixelbuffer.js is available on npm. To install it, run the following command:
```bash
    npm install pixelbuffer
```
## Usage
Pixelbuffer.js is designed to be used in the browser, but can also be used in Node.js. To use it in the browser, include the following script tag in your HTML file:
```html
    <script src="node_modules/pixelbuffer/dist/pixelbuffer.min.js"></script>
```
To use it in Node.js, include the following line at the top of your JavaScript file:
```js
var Pixelbuffer = require('pixelbuffer');      
```

## Examples
### Creating a pixel buffer
To create a pixel buffer, use the `Pixelbuffer` constructor. The constructor takes two arguments: the width and height of the pixel buffer. The following example creates a 100x100 pixel buffer:
```bash
    var pixelbuffer = new Pixelbuffer(100, 100);
```
### Getting and setting pixels
```js   
    var pixelbuffer = new Pixelbuffer(100, 100);
    pixelbuffer.setPixel(0, 0, 255, 0, 0, 255); // Set the pixel at (0, 0) to red
    var pixel = pixelbuffer.getPixel(0, 0); // Get the pixel at (0, 0)
```

# Usage with HTML5 Canvas

## Creating a pixel buffer from a canvas    

```js
    var canvas = document.getElementById('canvas');
    var pixelbuffer = Pixelbuffer.fromCanvas(canvas);
```

## Creating a canvas from a pixel buffer

```js
    var canvas = document.getElementById('canvas');
    var pixelbuffer = new Pixelbuffer(100, 100);
    pixelbuffer.toCanvas(canvas);
```

```js
    PixelBuffer.prototype.fromCanvas = function (canvas) {
      var ctx = canvas.getContext('2d');
      var imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);
      this.setImageData(imageData);
    }

    PixelBuffer.prototype.toCanvas = function (canvas) {
      var ctx = canvas.getContext('2d');
      ctx.putImageData(this.getImageData(), 0, 0);
    }
```