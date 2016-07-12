# Adafruit-8x8-Matrix-with-NodeJS

Controll your [Adafruit 8x8 Matrix](https://www.adafruit.com/products/959) with NodeJS.


## RPIO

[rpio](https://www.npmjs.com/package/rpio) is required for this library

```
npm install rpio
```

## Setup

Include rpio and 8x8matrix to your .js-file, initialize 8x8matrix with your rpio and start manipulatin pixels.

```
var rpio = require('rpio');
var matrix = require('8x8matrix');

matrix.init(rpio);
matrix.writeArray(matrix.smily);
```