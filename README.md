# @taktikorg/recusandae-quae <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS DataView? This module works cross-realm/iframe, does not depend on `instanceof` or mutable properties, and despite ES6 Symbol.toStringTag.

## Example

```js
var isDataView = require('@taktikorg/recusandae-quae');
var assert = require('assert');

assert.equal(false, isDataView(undefined));
assert.equal(false, isDataView(null));
assert.equal(false, isDataView(false));
assert.equal(false, isDataView(true));
assert.equal(false, isDataView([]));
assert.equal(false, isDataView({}));
assert.equal(false, isDataView(/a/g));
assert.equal(false, isDataView(new RegExp('a', 'g')));
assert.equal(false, isDataView(new Date()));
assert.equal(false, isDataView(42));
assert.equal(false, isDataView(NaN));
assert.equal(false, isDataView(Infinity));
assert.equal(false, isDataView(new Number(42)));
assert.equal(false, isDataView('foo'));
assert.equal(false, isDataView(Object('foo')));
assert.equal(false, isDataView(function () {}));
assert.equal(false, isDataView(function* () {}));
assert.equal(false, isDataView(x => x * x));
assert.equal(false, isDataView([]));
assert.equal(false, isDataView(new Int8Array()));
assert.equal(false, isDataView(new Uint8Array()));
assert.equal(false, isDataView(new Uint8ClampedArray()));
assert.equal(false, isDataView(new Int16Array()));
assert.equal(false, isDataView(new Uint16Array()));
assert.equal(false, isDataView(new Int32Array()));
assert.equal(false, isDataView(new Uint32Array()));
assert.equal(false, isDataView(new Float32Array()));
assert.equal(false, isDataView(new Float64Array()));
assert.equal(false, isDataView(new BigInt64Array()));
assert.equal(false, isDataView(new BigUint64Array()));

assert.ok(isDataView(new DataView(new ArrayBuffer(0))));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@taktikorg/recusandae-quae
[npm-version-svg]: https://versionbadg.es/inspect-js/@taktikorg/recusandae-quae.svg
[deps-svg]: https://david-dm.org/inspect-js/@taktikorg/recusandae-quae.svg
[deps-url]: https://david-dm.org/inspect-js/@taktikorg/recusandae-quae
[dev-deps-svg]: https://david-dm.org/inspect-js/@taktikorg/recusandae-quae/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@taktikorg/recusandae-quae#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@taktikorg/recusandae-quae.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@taktikorg/recusandae-quae.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@taktikorg/recusandae-quae.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@taktikorg/recusandae-quae
[codecov-image]: https://codecov.io/gh/inspect-js/@taktikorg/recusandae-quae/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@taktikorg/recusandae-quae/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@taktikorg/recusandae-quae
[actions-url]: https://github.com/taktikorg/recusandae-quae/actions
