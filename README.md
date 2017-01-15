# nkd 1.0.1

Barebones scaffolding for developing a jekyll site.

#### Stats

3593 | 174 | 161
---|---|---
bytes | selectors | declarations

## Installation

#### With [npm](https://npmjs.com)

```
npm install --save-dev nkd
```

#### With Git

```
git clone https://github.com/tachyons-css/nkd
```

## Usage

#### Using with [PostCSS](https://github.com/postcss/postcss)

Import the css module

```css
@import "nkd";
```

Then process the CSS using the [`tachyons-cli`](https://github.com/tachyons-css/tachyons-cli)

```sh
$ npm i -g tachyons-cli
$ tachyons-cli path/to/css-file.css > dist/t.css
```

#### Using the CSS

The built CSS is located in the `css` directory. It contains an unminified and minified version.
You can either cut and paste that css or link to it directly in your html.

```html
<link rel="stylesheet" href="path/to/module/css/nkd">
```

#### Development

The source CSS files can be found in the `src` directory.
Running `$ npm start` will process the source CSS and place the built CSS in the `css` directory.

## The CSS

```css
/* NKD */
/* Include all css partials you want compiled to nkd.css. */
/*
   VARIABLES
*/
/* Breakpoints */
/* Type Scale */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
/**
 * 1. Set default font family to sans-serif.
 * 2. Prevent iOS and IE text size adjust after device orientation change,
 *    without disabling user zoom.
 */
html { font-family: sans-serif; /* 1 */ -ms-text-size-adjust: 100%; /* 2 */ -webkit-text-size-adjust: 100%; /* 2 */ }
/**
 * Remove default margin.
 */
body { margin: 0; }
/* HTML5 display definitions
   ========================================================================== */
/**
 * Correct `block` display not defined for any HTML5 element in IE 8/9.
 * Correct `block` display not defined for `details` or `summary` in IE 10/11
 * and Firefox.
 * Correct `block` display not defined for `main` in IE 11.
 */
article, aside, details, figcaption, figure, footer, header, hgroup, main, menu,
nav, section, summary { display: block; }
/**
 * 1. Correct `inline-block` display not defined in IE 8/9.
 * 2. Normalize vertical alignment of `progress` in Chrome, Firefox, and Opera.
 */
audio, canvas, progress, video { display: inline-block; /* 1 */ vertical-align: baseline; /* 2 */ }
/**
 * Prevent modern browsers from displaying `audio` without controls.
 * Remove excess height in iOS 5 devices.
 */
audio:not([controls]) { display: none; height: 0; }
/**
 * Address `[hidden]` styling not present in IE 8/9/10.
 * Hide the `template` element in IE 8/9/10/11, Safari, and Firefox < 22.
 */
[hidden], template { display: none; }
/* Links
   ========================================================================== */
/**
 * Remove the gray background color from active links in IE 10.
 */
a { background-color: transparent; }
/**
 * Improve readability of focused elements when they are also in an
 * active/hover state.
 */
a:active, a:hover { outline: 0; }
/* Text-level semantics
   ========================================================================== */
/**
 * Address styling not present in IE 8/9/10/11, Safari, and Chrome.
 */
abbr[title] { border-bottom: 1px dotted; }
/**
 * Address style set to `bolder` in Firefox 4+, Safari, and Chrome.
 */
b, strong { font-weight: bold; }
/**
 * Address styling not present in Safari and Chrome.
 */
dfn { font-style: italic; }
/**
 * Address variable `h1` font-size and margin within `section` and `article`
 * contexts in Firefox 4+, Safari, and Chrome.
 */
h1 { font-size: 2em; margin: 0.67em 0; }
/**
 * Address styling not present in IE 8/9.
 */
mark { background: #ff0; color: #000; }
/**
 * Address inconsistent and variable font size in all browsers.
 */
small { font-size: 80%; }
/**
 * Prevent `sub` and `sup` affecting `line-height` in all browsers.
 */
sub, sup { font-size: 75%; line-height: 0; position: relative; vertical-align: baseline; }
sup { top: -0.5em; }
sub { bottom: -0.25em; }
/* Embedded content
   ========================================================================== */
/**
 * Remove border when inside `a` element in IE 8/9/10.
 */
img { border: 0; }
/**
 * Correct overflow not hidden in IE 9/10/11.
 */
svg:not(:root) { overflow: hidden; }
/* Grouping content
   ========================================================================== */
/**
 * Address margin not present in IE 8/9 and Safari.
 */
figure { margin: 1em 40px; }
/**
 * Address differences between Firefox and other browsers.
 */
hr { box-sizing: content-box; height: 0; }
/**
 * Contain overflow in all browsers.
 */
pre { overflow: auto; }
/**
 * Address odd `em`-unit font size rendering in all browsers.
 */
code, kbd, pre, samp { font-family: monospace, monospace; font-size: 1em; }
/* Forms
   ========================================================================== */
/**
 * Known limitation: by default, Chrome and Safari on OS X allow very limited
 * styling of `select`, unless a `border` property is set.
 */
/**
 * 1. Correct color not being inherited.
 *    Known issue: affects color of disabled elements.
 * 2. Correct font properties not being inherited.
 * 3. Address margins set differently in Firefox 4+, Safari, and Chrome.
 */
button, input, optgroup, select, textarea { color: inherit; /* 1 */ font: inherit; /* 2 */ margin: 0; /* 3 */ }
/**
 * Address `overflow` set to `hidden` in IE 8/9/10/11.
 */
button { overflow: visible; }
/**
 * Address inconsistent `text-transform` inheritance for `button` and `select`.
 * All other form control elements do not inherit `text-transform` values.
 * Correct `button` style inheritance in Firefox, IE 8/9/10/11, and Opera.
 * Correct `select` style inheritance in Firefox.
 */
button, select { text-transform: none; }
/**
 * 1. Avoid the WebKit bug in Android 4.0.* where (2) destroys native `audio`
 *    and `video` controls.
 * 2. Correct inability to style clickable `input` types in iOS.
 * 3. Improve usability and consistency of cursor style between image-type
 *    `input` and others.
 */
button, html input[type="button"], /* 1 */
input[type="reset"],
input[type="submit"] { -webkit-appearance: button; /* 2 */ cursor: pointer; /* 3 */ }
/**
 * Re-set default cursor for disabled elements.
 */
button[disabled], html input[disabled] { cursor: default; }
/**
 * Remove inner padding and border in Firefox 4+.
 */
button::-moz-focus-inner, input::-moz-focus-inner { border: 0; padding: 0; }
/**
 * Address Firefox 4+ setting `line-height` on `input` using `!important` in
 * the UA stylesheet.
 */
input { line-height: normal; }
/**
 * It's recommended that you don't attempt to style these elements.
 * Firefox's implementation doesn't respect box-sizing, padding, or width.
 *
 * 1. Address box sizing set to `content-box` in IE 8/9/10.
 * 2. Remove excess padding in IE 8/9/10.
 */
input[type="checkbox"], input[type="radio"] { box-sizing: border-box; /* 1 */ padding: 0; /* 2 */ }
/**
 * Fix the cursor style for Chrome's increment/decrement buttons. For certain
 * `font-size` values of the `input`, it causes the cursor style of the
 * decrement button to change from `default` to `text`.
 */
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button { height: auto; }
/**
 * 1. Address `appearance` set to `searchfield` in Safari and Chrome.
 * 2. Address `box-sizing` set to `border-box` in Safari and Chrome.
 */
input[type="search"] { -webkit-appearance: textfield; /* 1 */ box-sizing: content-box; /* 2 */ }
/**
 * Remove inner padding and search cancel button in Safari and Chrome on OS X.
 * Safari (but not Chrome) clips the cancel button when the search input has
 * padding (and `textfield` appearance).
 */
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration { -webkit-appearance: none; }
/**
 * Define consistent border, margin, and padding.
 */
fieldset { border: 1px solid #c0c0c0; margin: 0 2px; padding: 0.35em 0.625em 0.75em; }
/**
 * 1. Correct `color` not being inherited in IE 8/9/10/11.
 * 2. Remove padding so people aren't caught out if they zero out fieldsets.
 */
legend { border: 0; /* 1 */ padding: 0; /* 2 */ }
/**
 * Remove default vertical scrollbar in IE 8/9/10/11.
 */
textarea { overflow: auto; }
/**
 * Don't inherit the `font-weight` (applied by a rule above).
 * NOTE: the default cannot safely be changed in Chrome and Safari on OS X.
 */
optgroup { font-weight: bold; }
/* Tables
   ========================================================================== */
/**
 * Remove most spacing between table cells.
 */
table { border-collapse: collapse; border-spacing: 0; }
td, th { padding: 0; }
/* Resets */
/* Remove default styling on lists */
.list-reset { list-style: none; }
.input-reset { appearance: none; -webkit-appearance: none; -moz-appearance: none; }
/*
   TYPE

   - Fonts
   - Headers
   - Copy

*/
/*
  Font Stacks
*/
body, .sans-serif { font-family: -apple-system, "Avenir Next", Avenir, "Helvetica Neue", Helvetica, Roboto, Noto, Ubuntu, "franklin gothic", Arial, sans-serif; }
.serif { font-family: georgia, serif; }
/*
  Type Scale
*/
.f1 { font-size: 96px; }
.f2 { font-size: 62px; }
.f3 { font-size: 48px; }
.f4 { font-size: 32px; }
.f5 { font-size: 24px; }
.f6 { font-size: 19px; }
.f7 { font-size: 16px; }
/* Font Weights */
.fw1 { font-weight: 100; }
.fw2 { font-weight: 200; }
.fw3 { font-weight: 300; }
.fw4 { font-weight: 400; }
.fw5 { font-weight: 500; }
.fw6 { font-weight: 600; }
.fw7 { font-weight: 700; }
.fw8 { font-weight: 800; }
.fw9 { font-weight: 900; }
/* Measure */
.measure { max-width: 30em; }
/* Casing */
.caps { text-transform: uppercase; letter-spacing: 0.1em; }
.title-casing { text-transform: capitalize; }
/* Alignment */
.tr { text-align: right; }
.tl { text-align: left; }
.tc { text-align: center; }
/* Wrapping
   ========================================================================== */
.nowrap { white-space: nowrap; }
/* Leading
   ========================================================================== */
.lh-solid { line-height: 1; }
.lh-title { line-height: 1.3; }
.lh-copy { line-height: 1.6; }
/* */
.content p, .content blockquote, .content small { max-width: 30em; line-height: 1.5; }
.link { text-decoration: none; }
.dim { opacity: 1; transition: opacity .15s ease-in; }
.dim:focus, .dim:hover { opacity: .8; transition: opacity .15s ease-out; }
/* Spacing */
.pa0 { padding: 0; }
.pa1 { padding: .25rem; }
.pa2 { padding: .5rem; }
.pa3 { padding: 1rem; }
.pa4 { padding: 2rem; }
.pa5 { padding: 4rem; }
.pt0 { padding-top: 0; }
.pt1 { padding-top: .25rem; }
.pt2 { padding-top: .5rem; }
.pt3 { padding-top: 1rem; }
.pt4 { padding-top: 2rem; }
.pt5 { padding-top: 4rem; }
.pr0 { padding-right: 0; }
.pr1 { padding-right: .25rem; }
.pr2 { padding-right: .5rem; }
.pr3 { padding-right: 1rem; }
.pr4 { padding-right: 2rem; }
.pr5 { padding-right: 4rem; }
.pb0 { padding-bottom: 0; }
.pb1 { padding-bottom: .25rem; }
.pb2 { padding-bottom: .5rem; }
.pb3 { padding-bottom: 1rem; }
.pb4 { padding-bottom: 2rem; }
.pb5 { padding-bottom: 4rem; }
.pl0 { padding-left: 0; }
.pl1 { padding-left: .25rem; }
.pl2 { padding-left: .5rem; }
.pl3 { padding-left: 1rem; }
.pl4 { padding-left: 2rem; }
.pl5 { padding-left: 4rem; }
.ma0 { margin: 0; }
.ma1 { margin: .25rem; }
.ma2 { margin: .5rem; }
.ma3 { margin: 1rem; }
.ma4 { margin: 2rem; }
.ma5 { margin: 4rem; }
.mt0 { margin-top: 0; }
.mt1 { margin-top: .25rem; }
.mt2 { margin-top: .5rem; }
.mt3 { margin-top: 1rem; }
.mt4 { margin-top: 2rem; }
.mt5 { margin-top: 4rem; }
.mr0 { margin-right: 0; }
.mr1 { margin-right: .25rem; }
.mr2 { margin-right: .5rem; }
.mr3 { margin-right: 1rem; }
.mr4 { margin-right: 2rem; }
.mr5 { margin-right: 4rem; }
.mb0 { margin-bottom: 0; }
.mb1 { margin-bottom: .25rem; }
.mb2 { margin-bottom: .5rem; }
.mb3 { margin-bottom: 1rem; }
.mb4 { margin-bottom: 2rem; }
.mb5 { margin-bottom: 4rem; }
.ml0 { margin-left: 0; }
.ml1 { margin-left: .25rem; }
.ml2 { margin-left: .5rem; }
.ml3 { margin-left: 1rem; }
.ml4 { margin-left: 2rem; }
.ml5 { margin-left: 4rem; }
/*
   SITE STYLES
*/
/*
  Add your site styles here. Break things out to additional partials if you'd
  like and add inport them in nkd.css
*/
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Authors

* [mrmrs](http://mrmrs.io)
* [johno](http://johnotander.com)

## License

MIT

