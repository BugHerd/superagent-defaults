superagent-defaults [![Build Status](https://travis-ci.org/CamShaft/superagent-defaults.png)](https://travis-ci.org/CamShaft/superagent-defaults)
===================

Create some defaults for superagent requests

Usage
-----

```js
var defaults = require('superagent-defaults');

// Create a defaults context
var superagent = defaults();

// Setup some defaults
superagent
  .set('my-default-header', 'my-default-value')
  .on(function (req){
    console.log(req.url);
  });

// Use superagent like you always have; the defaults will be applied to
// each request automatically
superagent
  .get('/my-api')
  .end(function(res) {
    console.log(res.text);
  });
```

Tests
-----

```sh
$ npm test
```
