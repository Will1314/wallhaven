# wallhaven

[![NPM version](https://img.shields.io/npm/v/wallhaven.svg?style=flat)](https://npmjs.com/package/wallhaven) [![NPM downloads](https://img.shields.io/npm/dm/wallhaven.svg?style=flat)](https://npmjs.com/package/wallhaven) [![CircleCI](https://circleci.com/gh/egoist/wallhaven/tree/master.svg?style=shield)](https://circleci.com/gh/egoist/wallhaven/tree/master)  [![codecov](https://codecov.io/gh/egoist/wallhaven/branch/master/graph/badge.svg)](https://codecov.io/gh/egoist/wallhaven)
 [![donate](https://img.shields.io/badge/$-donate-ff69b4.svg?maxAge=2592000&style=flat)](https://github.com/egoist/donate)

## Install

```bash
yarn add wallhaven
```

## Usage

```js
const Wallhaven = require('wallhaven')

const api = new Wallhaven()

api.search('attack on titans')
  .then(result => {
    console.log(result)
    // => { totalPages: 29, images: [] }
  })
```

## Micro-service

A micro-service based on this module: https://wallhaven.now.sh

Examples: 

- Search: https://wallhaven.now.sh/search?keyword=attack%20on%20titans
- Details: https://wallhaven.now.sh/details/482373
- Random: https://wallhaven.now.sh/random?keyword=eriri

## API

### api.search(keyword, [options])

Search wallpapers by given keyword.

#### options.categories

Type: `Array`<br>
Default: `['general', 'anime', 'people']`

#### options.page

Type: `Number`<br>
Default: `1`

#### options.sorting

Type: `string`<br>
Default: `relevance`<br>
Value: one of `relevance` `random` `date_added` `views` `favorites`

#### options.nsfw

Type: `boolean`<br>
Default: `false`

Show NSFW (not safe for work) result.

#### options.sketchy

Type: `boolean`<br>
Default: `false`

Show sketchy wallpapers only.

### api.details(id)

Get the details of a wallpaper by image id.

#### id

Type: `Number`

Image ID.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D


## Author

**wallhaven** © [EGOIST](https://github.com/egoist), Released under the [MIT](./LICENSE) License.<br>
Authored and maintained by egoist with help from contributors ([list](https://github.com/egoist/wallhaven/contributors)).

> [Website](https://egoist.sh) · GitHub [@egoist](https://github.com/egoist) · Twitter [@_egoistlily](https://twitter.com/_egoistlily)
