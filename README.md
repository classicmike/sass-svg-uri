# SASS SVG URI

## Description
**NOTE**: This is **NOT** my original work. 

The intention of this repo is to port the original [waldemarfm/sass-svg-uri](https://github.com/waldemarfm/sass-svg-uri) to be supported in the Dart SASS implementation without it outputting any warnings and errors. The original repo is 'no longer being maintained' in that its version 1.0 did exactly what was on the tin and had no dependencies to justify additional maintenance.

### So what if I need to support SASS implementations before Dart SASS?
If you are after support for node-sass or SASS implementations **_before_** the Dart SASS implementation, please follow the link over here for the original [waldemarfm/sass-svg-uri](https://github.com/waldemarfm/sass-svg-uri) repository and the original [sass-svg-uri](https://www.npmjs.com/package/sass-svg-uri) npm package.

### Original Description Text
This is just a simple module with [Jakob Eriksen's function](http://codepen.io/jakob-e/pen/doMoML) for easy use in projects. Uses [Hugo Giraudel's str-replace function](http://sassmeister.com/gist/1b4f2da5527830088e4d) to replace invalid characters in the SVG as a data uri.

## Usage

Just import the file and use the function, no dependencies.

```scss
@import "@classicmike/sass-svg-uri/svg-uri";

.icon {
    background-image: svg-uri('<svg xmlns="http://www.w3.org/2000/svg"> ... </svg>');
}
```

Would output:

```css
.icon {
    background-image: url("data:image/svg+xml;charset=utf8,%3Csvg xmlns='http://www.w3.org/2000/svg'%3E% ... %3C/svg%3E");
}
```

To know more:

* [CSS-Tricks: Probably Don’t Base64 SVG](https://css-tricks.com/probably-dont-base64-svg/)
* [Codepen: Optimizing SVGs in data URIs](http://codepen.io/Tigt/post/optimizing-svgs-in-data-uris)

