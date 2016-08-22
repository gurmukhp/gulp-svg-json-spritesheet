# gulp-svg-json-spritesheet

> Using this plugin, you'll be able to compress SVGs into a JSON spritesheet file.


## Install

```
$ npm install --save-dev gulp-svg-spritesheet
```


## Usage

```js
var gulp = require('gulp');
var svg = require('gulp-svg-spritesheet');

gulp.task('default', function() {
  return gulp.src('svg/*.svg')
      .pipe(svg('compressed.json'))
      .pipe(gulp.dest('./'));
});
```

In the above example, all the SVGs in the image folder will be compressed and saved to compressed.json (sample output below).

### Sample Output

```json
{
  "fireplace_00000.svg": {
    "data": "<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"269\" height=\"393\" viewBox=\"0 0 269 393\">...</g></svg>",
    "info": {
      "width": "269",
      "height": "393"
    }
  },
  "fireplace_00001.svg": {
    "data": "<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"269\" height=\"393\" viewBox=\"0 0 269 393\">...</g></svg>",
    "info": {
      "width": "269",
      "height": "393"
    }
  }
}
```


## License

MIT © Gurmukh Panesar
