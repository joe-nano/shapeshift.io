shapeshift.io
=============

A JavaScript component for the crypto currency buying and selling shapeshift.io service. API
documentation here: https://shapeshift.io/api.html


Usage
-----

    npm i --save shapeshift.io


Methods
-------

### coins()

Get a map of supported coins.

Reference: https://shapeshift.io/api.html#getcoins

**Example:**

```js
var shapeshift = require('shapeshift.io')

shapeshift.coins(function (err, coinData) {
  console.dir(coinData) // =>
  /*
    { BTC:
     { name: 'Bitcoin',
       symbol: 'BTC',
       image: 'https://shapeshift.io/images/coins/bitcoin.png',
       status: 'available' },

       ...

    VRC:
     { name: 'Vericoin',
       symbol: 'VRC',
       image: 'https://shapeshift.io/images/coins/vericoin.png',
       status: 'available' } }
  */
})
```

### rate()

Get the exchange rate. Note, the `rate` is returned as a type of
`string`; this is to ensure precision matches the API exactly.

Reference: https://shapeshift.io/api.html#rate

**Example:**

```js
var shapeshift = require('shapeshift.io')

var pair = 'btc_ltc'
shapeshift.rate(pair, function (err, rate) {
  console.dir(rate) // => '158.71815287'
})
```


License
-------

MIT





