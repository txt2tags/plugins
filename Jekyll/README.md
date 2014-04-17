# Jekyll txt2tags plugin

Write your [Jekyll](http://jekyllrb.com) posts and pages using the [txt2tags](http://txt2tags.org) markup.


## Installation

Just copy the `txt2tags_converter.rb` file to the `_plugins` folder of your Jekyll website.

> Note: txt2tags must be installed on your machine ([get it](http://txt2tags.org/download.html)).


## Usage

All pages and posts files ending in the `.t2t` extension will be processed through txt2tags automatically.

Example:

	_posts/2014-01-10-hello-world.md
	_posts/2014-01-15-python.t2t
	_posts/2014-01-20-mac.t2t

The first post (`.md`) will be converted to HTML by Markdown, the others will use txt2tags.


## Post Example

	---
	title: My txt2tags test post
	layout: post
	---

	The first sentence, using [txt2tags http://tx2tags.org] markup.


## Have fun

The full power of txt2tags is available:

- Tables: easy and readable markup
- Automatic Table of Contents (TOC).
- Automatic numbering for lists and headings.
- Regex powered Pre and Post processing filters.

### Tables: easy and readable markup

	---
	title: Fruit colors
	layout: post
	---

	My preferred fruits and their colors:

	|| Fruit | Color  |
	| apple  | red    |
	| banana | yellow |
	| lemon  | green  |

### Automatic TOC and numbering

Long articles with lots of sections just beg for an automatic TOC and numbered headings.

	---
	title: My long article
	layout: post
	---

	% Inform extra command line options to txt2tags:
	%!options: --toc --toc-level 2 --enum-title

	Hello, this is my very very long article. There are 10
	sections talking about fruits:

	%%toc

	...

###  Regex powered Pre and Post processing filters

Modify your contents with search & replace filters, before and/or after the HTML conversion.

	---
	title: Filters are nice
	layout: post
	---

	% Replace "quotes" with “fancy quotes”
	%!preproc: '"(.*?)"'   '“\1”'

	The first post sentence, after the "config" above.
