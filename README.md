# ➹ Clean-mark

  > Convert a blog article into a clean Markdown text file.

  [![NPM Version][npm-image]][npm-url]
  [![NPM Downloads][downloads-image]][downloads-url]
  [![Standard Style Guide][style-image]][style-url]


### Example

For example, this article:

[![Original article](article-screen.png)](http://www.techradar.com/news/amd-vs-intel-the-16-core-showdown)

Is converted into this text file:

![Clean text](clean-screen.png)


### Installation

Simply install with yarn:

> yarn global add clean-mark

Or with npm:

> npm install clean-mark --global


### Usage

> clean-mark "http://some-website.com/some-fancy-article"

The article will be automatically named using the URL path name. In the case, above, the name will be `some-fancy-article.md`.


This project depends on the [A-Extractor](https://github.com/croqaz/a-extractor) project, a database of expressions used for extracting content from blogs and articles.


### Why ?

* to save interesting articles offline, in a highly readable text format
* Markdown is easy to export into a clean printable document
* it's easy to read on a tablet, or a Kidle (as it is, or in PDF)
* for offline text analysis of multiple articles, using machine learning / AI


### How ?

Implementation steps:

1. Downloads the content of a web page
1. Meta-scrape page details (title, author, date, etc)
1. Sanitizes the ugly HTML
1. Minifies the disinfected HTML
1. Converts the result into clean Markdown text


### Help

Clean-mark was tested on all major news sites. On some websites, the text, or links are cut from the article.
In this case, you have to manually edit the resulted text,

AND

raise an [issue on A-Extractor](https://github.com/croqaz/a-extractor/issues) with the link that doesn't work and I'll add it in the database, so that next time, the text will be extracted correctly.

My desired goals are:

1. Good text extraction
1. More useless text is preferred, instead of wrongly cutting from the actual article
1. Extracting media (images, videos, audio) is not that important
1. Extraction speed is not that important


### Similar tools

* [Original readability](http://ejucovy.github.io/readability)
* [Next readability](https://github.com/luin/readability)
* [Other proiect](https://github.com/olragon/node-readability)
* [Node read](https://github.com/bndr/node-read)
* [Mozilla's readability](https://github.com/mozilla/readability)
* [Python newspaper](https://github.com/codelucas/newspaper)

-----

### License

[MIT](LICENSE) (c) 2017 Cristi Constantin


[npm-image]: https://img.shields.io/npm/v/clean-mark.svg
[npm-url]: https://www.npmjs.com/package/clean-mark
[downloads-image]: https://img.shields.io/npm/dm/clean-mark.svg
[downloads-url]: https://npmjs.org/package/clean-mark
[style-image]: https://img.shields.io/badge/code_style-standard-brightgreen.svg
[style-url]: https://standardjs.com
