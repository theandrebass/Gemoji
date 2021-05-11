# Gemoji

[![Coverage][coverage-badge]][coverage]
[![Downloads][downloads-badge]][downloads]
[![Size][size-badge]][size]

Gemoji (**G**itHub **Emoji**) contains info (category, description, names, and
tags) on Emoji and GitHub “Gemoji” shortcodes. Emojis for Github use.

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
    emoji: '😀',
    names: ['grinning'],
    tags: ['smile', 'happy'],
    description: 'grinning face',
    category: 'Smileys & Emotion'
  },
  {
    emoji: '😃',
    names: ['smiley'],
    tags: ['happy', 'joy', 'haha'],
    description: 'grinning face with big eyes',
    category: 'Smileys & Emotion'
  },
  {
    emoji: '😄',
    names: ['smile'],
    tags: ['happy', 'joy', 'laugh', 'pleased'],
    description: 'grinning face with smiling eyes',
    category: 'Smileys & Emotion'
  },
  {
    emoji: '😁',
    names: ['grin'],
    tags: [],
    description: 'beaming face with smiling eyes',
    category: 'Smileys & Emotion'
  },
  {
    emoji: '😆',
    names: ['laughing', 'satisfied'],
    tags: ['happy', 'haha'],
    description: 'grinning squinting face',
    category: 'Smileys & Emotion'
  },
  // …
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
🐱
💩
```

### Get name

```js
import {emojiToName} from 'gemoji'

console.log(emojiToName['🐶'])
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

*   `emoji`: `string`, example: `😀`
*   `names`: `string[]`, example: `['grinning']`
*   `tags`: `string[]`, example: `['smile', 'happy']`
*   `description`: `string`, example: `grinning face`
*   `category`: `string`, example: `Smileys & Emotion`

### `nameToEmoji`

`Object.<string, string>` — map names (`100`) to emoji (`💯`).

### `emojiToName`

`Object.<string, string>` — map names (`😀`) to emoji (`grinning`).

## Supported Gemoji

See [support.md][support].

## Data

The emoji list is crawled from [`github/gemoji`][gh] and later processed for
relevant information.
See its [license][gh-license] for more information.

No images are included in this repository: the copyrighted material may or may
not be available on the users computer.

## License

[MIT][license] © [Andre Bass][author]

<!-- Definitions -->

[build-badge]: https://github.com/theandrebass/Gemoji/workflows/main/badge.svg

[build]: https://github.com/theandrebass/gemoji/actions

[coverage-badge]: https://img.shields.io/codecov/c/github/theandrebass/gemoji.svg

[coverage]: https://codecov.io/github/theandrebass/gemoji

[downloads-badge]: https://img.shields.io/npm/dm/gemoji.svg

[downloads]: https://www.npmjs.com/package/gemoji

[size-badge]: https://img.shields.io/bundlephobia/minzip/gemoji.svg

[size]: https://bundlephobia.com/result?p=gemoji

[npm]: https://docs.npmjs.com/cli/install

[license]: license

[author]: https://robertandrebass.com

[support]: support.md

[gh]: https://github.com/github/gemoji

[gh-license]: https://github.com/github/gemoji/blob/55a0080/LICENSE
