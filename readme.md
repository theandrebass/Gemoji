# gemoji

[![Build][build-badge]][build]
[![Coverage][coverage-badge]][coverage]
[![Downloads][downloads-badge]][downloads]
[![Size][size-badge]][size]

Gemoji (**G**itHub **Emoji**) contains info (category, description, names, and
tags) on Emoji and GitHub âGemojiâ shortcodes.

## Install

This package is ESM only: Node 12+ is needed to use it and it must be `import`ed
instead of `require`d.

[npm][]:

```sh
npm install gemoji
```

## Use

```js
import {gemoji} from 'gemoji'

console.log(gemoji)
```

Yields:

```js
[
  {
    emoji: 'ð',
    names: ['grinning'],
    tags: ['smile', 'happy'],
    description: 'grinning face',
    category: 'Smileys & Emotion'
  },
  {
    emoji: 'ð',
    names: ['smiley'],
    tags: ['happy', 'joy', 'haha'],
    description: 'grinning face with big eyes',
    category: 'Smileys & Emotion'
  },
  {
    emoji: 'ð',
    names: ['smile'],
    tags: ['happy', 'joy', 'laugh', 'pleased'],
    description: 'grinning face with smiling eyes',
    category: 'Smileys & Emotion'
  },
  {
    emoji: 'ð',
    names: ['grin'],
    tags: [],
    description: 'beaming face with smiling eyes',
    category: 'Smileys & Emotion'
  },
  {
    emoji: 'ð',
    names: ['laughing', 'satisfied'],
    tags: ['happy', 'haha'],
    description: 'grinning squinting face',
    category: 'Smileys & Emotion'
  },
  // â¦
]
```

### Get emoji

```js
import {nameToEmoji} from 'gemoji'

console.log(nameToEmoji.cat)
console.log(nameToEmoji.poop)
```

Yields:

```txt
ð±
ð©
```

### Get name

```js
import {emojiToName} from 'gemoji'

console.log(emojiToName['ð¶'])
console.log(emojiToName['\uD83D\uDCA9'])
```

Yields:

```txt
dog
hankey
```

## API

This package exports the following identifiers: `gemoji`, `nameToEmoji`,
`emojiToName`.
There is no default export.

### `gemoji`

`Info[]`, where each `Info` is `Object` with:

*   `emoji`: `string`, example: `ð`
*   `names`: `string[]`, example: `['grinning']`
*   `tags`: `string[]`, example: `['smile', 'happy']`
*   `description`: `string`, example: `grinning face`
*   `category`: `string`, example: `Smileys & Emotion`

### `nameToEmoji`

`Object.<string, string>` â map names (`100`) to emoji (`ð¯`).

### `emojiToName`

`Object.<string, string>` â map names (`ð`) to emoji (`grinning`).

## Supported Gemoji

See [support.md][support].

## Data

The emoji list is crawled from [`github/gemoji`][gh] and later processed for
relevant information.
See its [license][gh-license] for more information.

No images are included in this repository: the copyrighted material may or may
not be available on the users computer.

## Related

*   [`emoji-emotion`](https://github.com/words/emoji-emotion)
    â List of emoji rated for valence
*   [`emoticon`](https://github.com/wooorm/emoticon)
    â Info on ASCII emoticons
*   [`strip-skin-tone`](https://github.com/wooorm/strip-skin-tone)
    â Strip skin-tones from emoji
*   [`wooorm.com/checkmoji`](https://wooorm.com/checkmoji/)
    â Check emoji across platforms

## Disclaimer

`wooorm/gemoji` is not affiliated with **GitHub**.

## License

[MIT][license] Â© [Titus Wormer][author]

<!-- Definitions -->

[build-badge]: https://github.com/wooorm/gemoji/workflows/main/badge.svg

[build]: https://github.com/wooorm/gemoji/actions

[coverage-badge]: https://img.shields.io/codecov/c/github/wooorm/gemoji.svg

[coverage]: https://codecov.io/github/wooorm/gemoji

[downloads-badge]: https://img.shields.io/npm/dm/gemoji.svg

[downloads]: https://www.npmjs.com/package/gemoji

[size-badge]: https://img.shields.io/bundlephobia/minzip/gemoji.svg

[size]: https://bundlephobia.com/result?p=gemoji

[npm]: https://docs.npmjs.com/cli/install

[license]: license

[author]: https://wooorm.com

[support]: support.md

[gh]: https://github.com/github/gemoji

[gh-license]: https://github.com/github/gemoji/blob/55a0080/LICENSE
