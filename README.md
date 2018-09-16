# Adafruit 8x8-Matrix with NodeJS ![](https://img.shields.io/npm/v/8x8matrix.svg) ![](https://img.shields.io/bundlephobia/min/8x8matrix.svg) ![](https://img.shields.io/npm/dt/8x8matrix.svg)

Control your [Adafruit 8x8 Matrix](https://www.adafruit.com/products/959) with NodeJS.

## Setup

Include rpio and 8x8matrix to your .js-file, initialize 8x8matrix with your rpio and start manipulatin pixels.

```js
const Matrix = require('./8x8matrix');

let matrix = new Matrix();
matrix.writeArray(matrix.smily);
```

## Options 

```js
let matrix = new Matrix({
	brightness: 15,
	slaveAddress: 0x70,
	bautrate: 10000
});
```

## API

Pixels can be written by a simple js-array with 64 objects. 

```js
var smily = [
	0,0,1,1,1,1,0,0,
	0,1,0,0,0,0,1,0,
	1,0,1,0,1,0,0,1,
	1,0,1,0,1,0,0,1,
	1,0,0,0,0,1,0,1,
	1,0,1,1,1,0,0,1,
	0,1,0,0,0,0,1,0,
	0,0,1,1,1,1,0,0
];

matrix.writeArray(smily);
```

## Test

```
$ sudo node test.js
```