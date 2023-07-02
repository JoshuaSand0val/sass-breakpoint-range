# Responsive range resizing with configurable breakpoints.

**Add it to your project now via installation by NPM:**

```bash
$ npm install sass-breakpoint-range --save-dev
```

---

## What is SASS Breakpoint Range?
SASS Breakpoint Range is a simple range function (built in SASS/SCSS) that resizes values with configurable breakpoints.  
It is built upon CSS [container queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_container_queries) and [custom properties](https://developer.mozilla.org/en-US/docs/Web/CSS/--*).

## Get started using SASS Breakpoint Range!
### Getting started is easy! Just complete a few steps.

1. Open a terminal (in this case, Bash) and install via NPM.  
*If you are unfamiliar with NPM, here is an [installation guide](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm).*

```bash
$ npm install sass-breakpoint-range --save-dev
```

2. Make a new `_range.scss` file and forward the package.  
*You can optionally [configure any variables](https://sass-lang.com/documentation/at-rules/forward#configuring-modules) using `with()` in SASS.*

```scss
// Range: SASS Breakpoint Range @forward with !default parameters.
@forward "node_modules/sass-breakpoint-range/" with (
	// Container Query breakpoints:
	$range-breakpoints: (0px, 180px, 320px, 640px, 960px, 1280px, 1440px) !default,
	// CSS Custom Property name:
	$range-property: --range !default
);
```

3. Make a new `styles.scss` file and write CSS using the package.

```scss
// Styles: Stylesheet using range() function.
@use "range" as *;

h1 {
	// Syntax: range($start: <length>, $end: <length>);
	font-size: range(32px, 64px);
}
```

4. Compile using SASS.  
*If you are unfamiliar with SASS, here is an [installation guide](https://sass-lang.com/install).*

```bash
$ sass --no-source-map styles.scss styles.css
```

## Acknowledgment
SASS Breakpoint Range was built by Joshua Elijah Sandoval.

## License
SASS Breakpoint Range is distributed under the [MIT](https://choosealicense.com/licenses/mit/) License.