# Pixelbuffer.js
Pixelbuffer.js is a JavaScript library for manipulating pixel buffers. It is designed to be used in the browser, but can also be used in Node.js.

## Installation
Pixelbuffer.js is available on npm. To install it, run the following command:

    npm install pixelbuffer

## Usage
Pixelbuffer.js is designed to be used in the browser, but can also be used in Node.js. To use it in the browser, include the following script tag in your HTML file:

    <script src="node_modules/pixelbuffer/dist/pixelbuffer.min.js"></script>

To use it in Node.js, include the following line at the top of your JavaScript file:
    
        var Pixelbuffer = require('pixelbuffer');   

## Examples
### Creating a pixel buffer
To create a pixel buffer, use the `Pixelbuffer` constructor. The constructor takes two arguments: the width and height of the pixel buffer. The following example creates a 100x100 pixel buffer:

    var pixelbuffer = new Pixelbuffer(100, 100);

### Getting and setting pixels

    var pixelbuffer = new Pixelbuffer(100, 100);
    pixelbuffer.setPixel(0, 0, 255, 0, 0, 255); // Set the pixel at (0, 0) to red
    var pixel = pixelbuffer.getPixel(0, 0); // Get the pixel at (0, 0)
