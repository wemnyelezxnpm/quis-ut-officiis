# @wemnyelezxnpm/quis-ut-officiis <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS Map? This module works cross-realm/iframe, and despite ES6 @@toStringTag.

## Example

```js
var isMap = require('@wemnyelezxnpm/quis-ut-officiis');
assert(!isMap(function () {}));
assert(!isMap(null));
assert(!isMap(function* () { yield 42; return Infinity; });
assert(!isMap(Symbol('foo')));
assert(!isMap(1n));
assert(!isMap(Object(1n)));

assert(!isMap(new Set()));
assert(!isMap(new WeakSet()));
assert(!isMap(new WeakMap()));

assert(isMap(new Map()));

class MyMap extends Map {}
assert(isMap(new MyMap()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@wemnyelezxnpm/quis-ut-officiis
[npm-version-svg]: https://versionbadg.es/inspect-js/@wemnyelezxnpm/quis-ut-officiis.svg
[deps-svg]: https://david-dm.org/inspect-js/@wemnyelezxnpm/quis-ut-officiis.svg
[deps-url]: https://david-dm.org/inspect-js/@wemnyelezxnpm/quis-ut-officiis
[dev-deps-svg]: https://david-dm.org/inspect-js/@wemnyelezxnpm/quis-ut-officiis/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@wemnyelezxnpm/quis-ut-officiis#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@wemnyelezxnpm/quis-ut-officiis.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@wemnyelezxnpm/quis-ut-officiis.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@wemnyelezxnpm/quis-ut-officiis.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@wemnyelezxnpm/quis-ut-officiis
[codecov-image]: https://codecov.io/gh/inspect-js/@wemnyelezxnpm/quis-ut-officiis/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@wemnyelezxnpm/quis-ut-officiis/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@wemnyelezxnpm/quis-ut-officiis
[actions-url]: https://github.com/wemnyelezxnpm/quis-ut-officiis/actions
