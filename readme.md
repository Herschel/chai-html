# Chai HTML ![Build status](https://api.travis-ci.org/i-like-robots/chai-html.png)

HTML assertions plugin for [Chai](http://chaijs.com/).

## Installation

```bash
npm install --save-dev chai-html
```

## Usage

```js
const chai      = require('chai')
const expect    = require('chai').expect
const chaiHtml  = require('chai-html')

// Register the plugin
chai.use(chaiHtml)

// Write assertions!
expect('<div><img /></div>').html.to.equal('<div><img></div>')
```

## How does it work?

The plugin uses [htmlparser2](https://www.npmjs.com/package/htmlparser2) to parse the given HTML strings and compares the generated trees using the `deep.equal` assertion.
