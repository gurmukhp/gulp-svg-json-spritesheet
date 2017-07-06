# gulp-svg-json-spritesheet

> Using this plugin, you'll be able to compress SVGs into a JSON spritesheet file.


## Install

```
$ npm install --save-dev gulp-svg-json-spritesheet
```


## Usage

```js
var gulp = require('gulp');
var svg = require('gulp-svg-json-spritesheet');

gulp.task('default', function() {
  return gulp.src('svg/*.svg')
      .pipe(svg('compressed.json', {
         prefix: '/images/,
         svgo: {
           // default svgo options go here  
         },
         showFilePath: true
       }))
      .pipe(gulp.dest('./'));
});
```

In the above example, all the SVGs in the image folder will be compressed and saved to compressed.json (sample output below).

### Options

#### prefix
Prefix the file name in the output.

#### svgo
An object of [options](https://github.com/svg/svgo#what-it-can-do) to use for SVGO.

#### showFilePath
Boolean of whether the full image file path should be added to the output.


## Sample Output

```json
{
  "/images/fireplace_00000.svg": {
    "data": "<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"269\" height=\"393\" viewBox=\"0 0 269 393\">...</g></svg>",
    "info": {
      "width": "269",
      "height": "393"
    }
  },
  "/images/fireplace_00001.svg": {
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
