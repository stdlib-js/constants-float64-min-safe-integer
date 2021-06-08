<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# Min Safe Integer

> Minimum safe [double-precision floating-point][ieee754] integer.

<section class="installation">

## Installation

```bash
npm install @stdlib/constants-float64-min-safe-integer
```

</section>

<section class="usage">

## Usage

```javascript
var FLOAT64_MIN_SAFE_INTEGER = require( '@stdlib/constants-float64-min-safe-integer' );
```

#### FLOAT64_MIN_SAFE_INTEGER

The minimum [safe][safe-integers] [double-precision floating-point][ieee754] integer.

```javascript
var bool = ( FLOAT64_MIN_SAFE_INTEGER === -9007199254740991 );
// returns true
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var randu = require( '@stdlib/random-base-randu' );
var round = require( '@stdlib/math-base-special-round' );
var pow = require( '@stdlib/math-base-special-pow' );
var FLOAT64_MIN_SAFE_INTEGER = require( '@stdlib/constants-float64-min-safe-integer' );

var min;
var x;
var i;

min = -pow( 2.0, 55 );
for ( i = 0; i < 100; i++ ) {
    x = round( randu() * min );
    if ( x < FLOAT64_MIN_SAFE_INTEGER ) {
        console.log( 'Unsafe: %d', x );
    } else {
        console.log( 'Safe: %d', x );
    }
}
```

</section>

<!-- /.examples -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/constants-float64-min-safe-integer/main/LICENSE

[safe-integers]: http://www.2ality.com/2013/10/safe-integers.html

[ieee754]: https://en.wikipedia.org/wiki/IEEE_754-1985

</section>

<!-- /.links -->
