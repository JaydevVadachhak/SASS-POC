# SASS - POC

### Node Package Manager

```bash
# Node should be installed

$npm init
```

### Gulp CLI Installation (Globally)

```bash
$npm install -g gulp-cli
```

### Gulp Installation (Locally)

```bash
$npm install gulp
$npm install gulp-sass
$npm install sass

or

$npm install gulp gulp-sass sass --save-dev
```

### gulpfile Setup

```javascript
const { src, dest, watch, series } = require("gulp");
const sass = require("gulp-sass")(require("sass"));

function buildStyles() {
  // dest() -> Write your .css dest folder here
  return src(`*.scss`).pipe(sass()).pipe(dest(`styles`));
}

function watchTask() {
  watch([`*.scss`], buildStyles);
}

exports.default = series(buildStyles, watchTask);
```

### Run Gulp

```bash
$gulp
```
