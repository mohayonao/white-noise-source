# WHITE NOISE SOURCE
[![Build Status](http://img.shields.io/travis/mohayonao/white-noise-source.svg?style=flat-square)](https://travis-ci.org/mohayonao/white-noise-source)
[![NPM Version](http://img.shields.io/npm/v/@mohayonao/white-noise-source.svg?style=flat-square)](https://www.npmjs.org/package/@mohayonao/white-noise-source)
[![License](http://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](http://mohayonao.mit-license.org/)

> WhiteNoiseSourceNode for Web Audio API

## Installation

Node.js

```sh
npm install @mohayonao/white-noise-source
```

Browser

- [white-noise-source.js](https://raw.githubusercontent.com/mohayonao/white-noise-source/master/build/white-noise-source.js)

## Example

```js
import WhiteNoiseSource from "@mohayonao/white-noise-source";

let audioContext = new AudioContext();
let whiteNoise = new WhiteNoiseSource(audioContext);

whiteNoise.start();
whiteNoise.connect(audioContext.destination);

setTimeout(() => {
  whiteNoise.stop();
  whiteNoise.disconnect();
}, 1000);
```

## API
### WhiteNoiseSource
- `constructor(audioContext: AudioContext)`

#### Instance attributes
- `context: AudioContext` _readonly_
- `onended: function`

#### Instance methods
- `start(when: number = 0): void`
- `stop(when: number = 0): void`
- `connect(...args): void`
- `disconnect(...args): void`
- `dispose(): void`

## LICENSE
MIT
