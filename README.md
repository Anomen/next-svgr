# :rocket: next-svgr

[![License](https://img.shields.io/npm/l/@svgr/core.svg)](https://github.com/smooth-code/svgr/blob/master/LICENSE)
[![npm package](https://img.shields.io/npm/v/next-svgr/latest.svg)](https://www.npmjs.com/package/next-svgr)
[![Dependencies](https://img.shields.io/david/anomen/next-svgr.svg)](https://david-dm.org/anomen/next-svgr)
[![DevDependencies](https://img.shields.io/david/dev/anomen/next-svgr.svg)](https://david-dm.org/anomen/next-svgr?type=dev)

Plugin for Next to automatically be able to transform `svg` files into components using the excellent [`svgr`](https://github.com/smooth-code/svgr) library.

## Table of contents

- [Installation](#installation)
- [Usage](#usage)

## Installation

```bash
npm install --save next-svgr
```

Or using yarn:

```bash
yarn add next-svgr
```

Then, import the library in your `next.config.js` file.

```js
// next.config.js
const withSvgr = require("next-svgr");

module.exports = withSvgr({
  // your config for other plugins or the general next.js here...
});
```

Or you can use it with [`next-compose-plugins`](https://github.com/cyrilwanner/next-compose-plugins) for a cleaner configuration.

```js
// next.config.js
const withPlugins = require("next-compose-plugins");
const withSvgr = require("next-svgr");

module.exports = withPlugins([
  withSvgr
  // your other plugins here
]);
```

## Usage

You can now start importing your SVG files as if they were components:

```js
import MyIcon from "./myicon.svg";

export default () => (
  <div>
    <MyIcon />
  </div>
);
```

Please check the [documentation of svgr for more examples](https://github.com/smooth-code/svgr).
