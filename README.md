# xy-parser

[![NPM version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]
[![Test coverage][codecov-image]][codecov-url]
[![npm download][download-image]][download-url]

Parse a text-file and convert it to an array of XY points.

## Installation

`$ npm install --save xy-parser`

## Usage

```js
import { parseXY } from "xy-parser";
const data = `My file
1   2
3   4
5   6
7   8`;
const result = parseXY(data);
/* result ->
    {
      x: [1, 3, 5, 7],
      y: [2, 4, 6, 8]
    }
  }
*/

const result2 = parseXY(data, { keepInfo: true });
/* result2 ->
    data: {
      x: [1, 3, 5, 7],
      y: [2, 4, 6, 8]
    },
    info: [
      'My file'
    ]
  }
*/
```

## [API Documentation](https://cheminfo.github.io/xy-parser/)

## License

[MIT](./LICENSE)

[npm-image]: https://img.shields.io/npm/v/xy-parser.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/xy-parser
[travis-image]: https://img.shields.io/travis/cheminfo/xy-parser/master.svg?style=flat-square
[travis-url]: https://travis-ci.org/cheminfo/xy-parser
[codecov-image]: https://img.shields.io/codecov/c/github/cheminfo/xy-parser.svg?style=flat-square
[codecov-url]: https://codecov.io/gh/cheminfo/xy-parser
[download-image]: https://img.shields.io/npm/dm/xy-parser.svg?style=flat-square
[download-url]: https://www.npmjs.com/package/xy-parser
