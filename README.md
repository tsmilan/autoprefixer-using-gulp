# Autoprefixer

A sample project file using autoprefixer with gulp.

## Usage

### The tasks in `gulpfile.js`:

```javascript
var gulp = require('gulp');
var autoprefixer = require('gulp-autoprefixer');

gulp.task('styles', function () {
  return gulp.src('css/styles.css')
  .pipe(autoprefixer('last 2 version'))
  .pipe(gulp.dest('build'))
});

gulp.task('watch', function() {
  gulp.watch('css/styles.css', gulp.series('styles'));
});
```
### Use `gulp watch` to automatically run the autoprefixer when the css file gets modified.


