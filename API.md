## `distance`

Get the interval between two pitches

If one or both are pitch classes, a simple ascending interval is returned

This function can be partially applied (see examples)

### Parameters

* `from` **`String or Array`** the first note
* `to` **`String or Array`** the other note


### Examples

```js
var distance = require('tonal.distance')
distance('C2', 'D3') // => '9M'
distance('D2', 'C2') // => '-2M'
distance('D', 'C') // => '7m'
```
```js
// partially applied
var fromC = distance('C')
fromC('D') // => '2M'
```

Returns  the interval between them


