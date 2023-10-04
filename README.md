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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Mode

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Pareto (Type I)][pareto-distribution] distribution [mode][mode].

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

The [mode][mode] for a [Pareto (Type I)][pareto-distribution] random variable with shape parameter `α > 0` and scale parameter `β > 0` is

<!-- <equation class="equation" label="eq:pareto_type1_mode" align="center" raw="\operatorname{mode}\left( X \right) = \beta" alt="Mode for a Pareto (Type I) distribution."> -->

```math
\mathop{\mathrm{mode}}\left( X \right) = \beta
```

<!-- <div class="equation" align="center" data-raw-text="\operatorname{mode}\left( X \right) = \beta" data-equation="eq:pareto_type1_mode">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@51534079fef45e990850102147e8945fb023d1d0/lib/node_modules/@stdlib/stats/base/dists/pareto-type1/mode/docs/img/equation_pareto_type1_mode.svg" alt="Mode for a Pareto (Type I) distribution.">
    <br>
</div> -->

<!-- </equation> -->

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import mode from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-pareto-type1-mode@esm/index.mjs';
```
The previous example will load the latest bundled code from the esm branch. Alternatively, you may load a specific version by loading the file from one of the [tagged bundles](https://github.com/stdlib-js/stats-base-dists-pareto-type1-mode/tags). For example,

```javascript
import mode from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-pareto-type1-mode@v0.1.1-esm/index.mjs';
```

#### mode( alpha, beta )

Returns the [mode][mode] of a [Pareto (Type I)][pareto-distribution] distribution with parameters `alpha` (shape parameter) and `beta` (scale parameter).

```javascript
var v = mode( 2.0, 1.0 );
// returns 1.0

v = mode( 4.0, 12.0 );
// returns 12.0

v = mode( 8.0, 2.0 );
// returns 2.0
```

If provided `NaN` as any argument, the function returns `NaN`.

```javascript
var v = mode( NaN, 2.0 );
// returns NaN

v = mode( 2.0, NaN );
// returns NaN
```

If provided `alpha <= 0`, the function returns `NaN`.

```javascript
var v = mode( 0.0, 1.0 );
// returns NaN

v = mode( -1.0, 1.0 );
// returns NaN
```

If provided `beta <= 0`, the function returns `NaN`.

```javascript
var v = mode( 1.0, 0.0 );
// returns NaN

v = mode( 1.0, -1.0 );
// returns NaN
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import randu from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@esm/index.mjs';
import EPS from 'https://cdn.jsdelivr.net/gh/stdlib-js/constants-float64-eps@esm/index.mjs';
import mode from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-pareto-type1-mode@esm/index.mjs';

var alpha;
var beta;
var v;
var i;

for ( i = 0; i < 10; i++ ) {
    alpha = ( randu()*10.0 ) + EPS;
    beta = ( randu()*10.0 ) + EPS;
    v = mode( alpha, beta );
    console.log( 'α: %d, β: %d, mode(X;α,β): %d', alpha.toFixed( 4 ), beta.toFixed( 4 ), v.toFixed( 4 ) );
}

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-pareto-type1-mode.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-pareto-type1-mode

[test-image]: https://github.com/stdlib-js/stats-base-dists-pareto-type1-mode/actions/workflows/test.yml/badge.svg?branch=v0.1.1
[test-url]: https://github.com/stdlib-js/stats-base-dists-pareto-type1-mode/actions/workflows/test.yml?query=branch:v0.1.1

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-pareto-type1-mode/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-pareto-type1-mode?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-pareto-type1-mode.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-pareto-type1-mode/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-base-dists-pareto-type1-mode/tree/deno
[umd-url]: https://github.com/stdlib-js/stats-base-dists-pareto-type1-mode/tree/umd
[esm-url]: https://github.com/stdlib-js/stats-base-dists-pareto-type1-mode/tree/esm
[branches-url]: https://github.com/stdlib-js/stats-base-dists-pareto-type1-mode/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-pareto-type1-mode/main/LICENSE

[pareto-distribution]: https://en.wikipedia.org/wiki/Pareto_distribution

[mode]: https://en.wikipedia.org/wiki/Mode_%28statistics%29

</section>

<!-- /.links -->
