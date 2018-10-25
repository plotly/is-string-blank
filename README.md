# is-string-blank

The fast way to check if a JS string is blank?

### Install

```
npm install is-string-blank
```

### API

```js
var isNumeric = require('is-string-blank');

isNumeric(/* any JS object */);
```

### Warning

Please look up the test cases in
[test.js](https://github.com/plotly/is-string-blank/blob/master/test.js) before
using this module.

Most importantly, `is-string-blank` returns false on number and string
constructors. That is, `isNumeric(new Number(1))` and `isNumeric(new
String('1'))` are **false**.

### Why?

In [plotly](https://plot.ly/)'s javascript graphing library
[plotly.js](https://plot.ly/javascript/) blank strings should be identified to be ignored e.g. by webgl. 
`is-string-blank` is
significantly simplified and sped up by ignoring number and string constructors.

### Author

Alex Johnson | https://github.com/alexcjohnson

### License

Copyright (c) 2015 Alex Johnson Released under the MIT license.
