# Vrex

**Enhanced Path2D wrapper for HTML Canvas** – adds `toPathData()` export, SVG path string generation, and keeps full compatibility with the native `Path2D` API.

## Features
- Works exactly like native `Path2D`
- Records all drawing commands into `pathData`
- Export as SVG path string with `.toPathData()`
- Supports all native `Path2D` methods
- Works in browser and Node.js (UMD build)
- Can replace native `Path2D` globally in browser

## Installation

**NPM**
```bash
npm install vrex
```

**Browser (Vanilla)**
```html
<script src="vrex.js"></script>
```

## Usage

### Node.js / Bundler
```js
const Vrex = require('vrex');

const path = new Vrex();
path.moveTo(10, 10);
path.lineTo(100, 100);
console.log(path.toPathData()); // M10 10 L100 100
```

### Vanilla Browser
```html
<script src="vrex.js"></script>
<script>
const path = new Path2D();
path.arc(50, 50, 25, 0, Math.PI * 2);
console.log(path.toPathData());
</script>
```

## Replace Native Path2D
In browser builds, Vrex **automatically replaces** the native `Path2D`, so all existing code gains `toPathData()`.

## API
Same as [CanvasRenderingContext2D Path2D](https://developer.mozilla.org/en-US/docs/Web/API/Path2D), plus:

### `toPathData()`
Returns the recorded SVG path string.

## License
Published under MIT License
