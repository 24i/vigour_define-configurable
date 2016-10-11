# define-configurable
Defines new (or modifies existing) properties (using [`Object.defineProperty`](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty)) on an object passed to `define` as `this`, setting `configurable: true` by default

[![Build Status](https://travis-ci.org/vigour-io/define-configurable.svg?branch=master)](https://travis-ci.org/vigour-io/define-configurable)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/)
[![npm version](https://badge.fury.io/js/define-configurable.svg)](https://badge.fury.io/js/define-configurable)
[![Coverage Status](https://coveralls.io/repos/github/vigour-io/define-configurable/badge.svg?branch=master)](https://coveralls.io/github/vigour-io/define-configurable?branch=master)

--
**Usage**

```javascript
const define = require('vigour-util/define')
const subject = {}
const props = [
  { one: true },
  { two: function () {
      console.log('do nothing')
    }
  }
]
define.apply(subject, props)
```