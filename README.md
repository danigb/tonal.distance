# tonal.distance

[![Build Status](https://travis-ci.org/danigb/tonal.svg?branch=master)](https://travis-ci.org/danigb/tonal.distance)
[![Code Climate](https://codeclimate.com/github/danigb/tonal.distance/badges/gpa.svg)](https://codeclimate.com/github/danigb/tonal.distance)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](https://github.com/feross/standard)
[![npm version](https://img.shields.io/npm/v/tonal.distance.svg)](https://www.npmjs.com/package/tonal.distance)
[![license](https://img.shields.io/npm/l/tonal.distance.svg)](https://www.npmjs.com/package/tonal.distance)
[![tonal](https://img.shields.io/badge/lib-tonal-yellow.svg)](https://www.npmjs.com/package/tonal)


`tonal.distance` is a function to get the interval distance between two pitches:

```js
var distance = require('tonal.distance')
distance('C3', 'E4') // => '3M'
```

## Install

Only via npm: `npm i --save tonal.distance`

## Usage

There's only one function with two params. The function can be partially applied:

```js
var fromC = distance('C4')
fromC('Eb3') // => '3m'
```

#### Get interval between two notes (pitches)

This is the simplest use case. Can be descending intervals:

```js
distance('C3', 'F3') // => '4P'
distance('C3', 'F2') // => '-5P'
```

#### Get interval between two pitch classes

If one or both pitches are pitch classes (no octave) an ascending interval is always returned:

```js
distance('C', 'F') // => '4P'
distance('B', 'C') // => '2m'
```

#### Subtract two intervals

It can be used to subtract intervals:

```js
distance('3M', '5P') // => '3m'
```

## License

MIT License
