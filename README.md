[![NPM Version](https://img.shields.io/npm/v/%40teampimcserver%2Fhexo-reading-time.svg)](https://www.npmjs.com/package/%40teampimcserver%2Fhexo-reading-time)

# hexo-reading-time
[Hexo](https://hexo.io/) plugin that displays reading time for the article.

## CHANGE

- Change to Japanese
- Change README.md
- Change Package.json

## Installation

```shell
#npm
npm install --save @teampimcserver/hexo-reading-time

#yarn
yarn add @teampimcserver/hexo-reading-time
```

## Usage
### Basic Usage

To display reading time, add the function into `post.ejs`.

Ejs:
```
<%- readingTime(page.content) %>
```
Swig:
```
{{ readingTime(page.content) }}
```
Jade:
```
span= readingTime(page.content)
```

It will display `X min. read`.

### Customization

You can customize the output by passing additional arguments.

Ejs:
```
<%- readingTime(page.content, 'min.', wordsperminute) %>
```
Swig:
```
{{ readingTime(page.content, 'min.', wordsperminute) }}
```
Jade:
```
span= readingTime(page.content, 'min.', wordsperminute)
```

Where:
 `'min.'` - second argument - any string that represents suffix. Default is 'min. read'
 `wpm` - number - words per minute. Default is 150.
 Both arguments are optional.

## License
MIT
