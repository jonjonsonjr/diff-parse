# diff-parse

> Unified diff parser for nodejs

This is straight from [parse-diff](https://github.com/sergeyt/parse-diff). I just compiled the coffeescript to javascript because coffeescript complicates things if you just want to use the module.

## JavaScript Usage Example

```javascript
var parse = require('diff-parse');
var diff = ''; // input diff string
var files = parse(diff);
console.log(files.length); // number of patched files
files.forEach(function(file) {
	console.log(file.lines.length); // number of hunk/added/deleted lines
	// each line in file.lines is a string
	console.log(file.deletions); // number of deletions in the patch
	console.log(file.additions); // number of additions in the patch
});
```
