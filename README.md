# define-configurable
Defines new (or modifies existing) properties Object.defineProperty on an object passed to define as this, setting configurable by default

[![Build Status](https://travis-ci.org/vigour-io/define-configurable.svg?branch=master)](https://travis-ci.org/vigour-io/define-configurable)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/)
[![npm version](https://badge.fury.io/js/define-configurable.svg)](https://badge.fury.io/js/define-configurable)
[![Coverage Status](https://coveralls.io/repos/github/vigour-io/define-configurable/badge.svg?branch=master)](https://coveralls.io/github/vigour-io/define-configurable?branch=master)

--

**Simple**

```javascript
const define = require('define-configurable')
const subject = {}
const props = [
  { one: true },
  { two () {
      console.log('do nothing')
    }
  }
]
define.apply(subject, props)
```

**Extend**

```javascript
const define = require('define-configurable')
const subject = {
  search (arg) {}
}

define.apply(subject, {
  extend: {
    // optmized method for extending up till 7 arguments
    search (method, arg) {
      return method.call(this, arg)
    }
  }
})
```
