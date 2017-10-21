# Changelog

## 1.4.3

**Release Date:** 2017-10-21

- Avoid unnecessary reentrancy in `doItalicsAndBold`.
- Reset the state for regular emphasis when unwinding in `toItalicsAndBold`.

## 1.4.2

**Release Date:** 2017-07-08

Added the `hashtag_protection` configuration variable. When `true`, prevents
ATX-style headers with no space after the initial hash from being interpreted as
headers. This way those precious hash-tags can be preserved.

## 1.4.1

**Release Date:** 2016-10-30

- Fixed a Markdown Extra issue where two-space-at-end-of-line hard breaks
  wouldn't work inside of HTML block elements such as `<p markdown="1">` where
  the element expects only span-level content.

## 1.4.0

**Release Date:** 2016-09-05

- [PHP Markdown settings](https://michelf.ca/projects/php-markdown/configuration/)
  can now be specified in the `config/markdown.php` config file.

## 1.3.8

**Release Date:** 2016-09-04

- Added a `hard_wrap` configuration variable to make all newline characters in
  the text become `<br>` tags in the HTML output. By default, according to the
  standard Markdown syntax these newlines are ignored unless they a preceded by
  two spaces. Thanks to Jonathan Cohlmeyer for the implementation.

## 1.3.7

**Release Date:** 2016-03-26

- Allow custom content function for code span. Just like the option
  `$code_block_content_func`, but now for code-span. Can be used to prevent the
  default `htmlspecialchars` or do some kind of other logic to convert the code
  to html.

## 1.3.6

**Release Date:** 2015-12-29

- Fixed an issue in MarkdownExtra where long header lines followed by a special
  attribute block would hit the backtrack limit an cause an empty string to be
  returned.
- Run [PHP CS Fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer) rules (PSR2 + Symfony).

## 1.3.5

**Release Date:** 2015-10-17

- The curled arrow character for the backlink in footnotes is now followed by a
  Unicode variant selector to prevent it from being displayed in emoji form on
  iOS. Note that in older browsers the variant selector is often interpreted as
  a separate character, making it visible after the arrow. So there is now a
  also a `fn_backlink_html` configuration variable that can be used to set the
  link text to something else.

## 1.3.4

**Release Date:** 2015-08-08

- You can now set a class name for the code block's language before the special
  attribute block. Previously, this class name was only allowed in the absence
  of the special attribute block.
- Added a `code_block_content_func` configuration variable which takes a
  function that will convert the content of the code block to HTML. This is most
  useful for syntax highlighting. For fenced code blocks in Markdown Extra, the
  function has access to the language class name (the one outside of the special
  attribute block). Credits to Mario Konrad for providing the implementation.
- Convert private members and methods to protected to allow inheritance.
- Update code header.

## 1.3.3

**Release Date:** 2015-06-13

- Reduce nesting in parse functions.
- Minor whitespace adjustments.

## 1.3.2

**Release Date:** 2015-03-29

**Merge PHP Markdown v1.5.0 Changes**

- Added the ability start ordered lists with a number different from 1 and and
  have that reflected in the HTML output. This can be enabled with the
  `enhanced_ordered_lists` configuration variable for the Markdown parser; it
  is enabled by default for Markdown Extra. Credits to Matt Gorle for
  providing the implementation.
- Added the ability to insert custom HTML attributes with simple values
  everywhere an extra attribute block is allowed (links, images, headers). The
  value must be unquoted, cannot contains spaces and is limited to
  alphanumeric ASCII characters. Credits to Peter Droogmans for providing the
  implementation.
- Added a `header_id_func` configuration variable which takes a function that
  can generate an `id` attribute value from the header text. Credits to Evert
  Pot for providing the implementation.
- Added a `url_filter_func` configuration variable which takes a function that
  can rewrite any link or image URL to something different.

## 1.3.1

**Release Date:** 2015-01-09

- Remove passing instance references to callbacks.

## 1.3.0

**Release Date:** 2014-12-30

- Bake in [PHP Markdown Extra](https://michelf.ca/projects/php-markdown/extra/).

## 1.2.2

**Release Date:** 2014-12-29

- Add Doc Blocks comments.

## 1.2.1

**Release Date:** 2014-12-27

- Whitespace clean-up.
- Remove legacy class constructor.

## 1.2.0

**Release Date:** 2012-10-20

- Rename `parse_markdown()` and `parse_markdown_file()` to `parse()` and `parse_file()`.
- Ensure file is readable in `parse_file()`.
- Whitespace clean-up.

## 1.1.0

**Release Date:** 2012-10-14

- Rename `Markdown_Parser` class to `Markdown`.
- Remove *WordPress* interface.
- Remove *Smarty* interface.
- Remove *Textile* interface.
- Remove *BBLOG* interface.
- Use HTML5 empty tags.
- Remove constant declarations.
- Move all properties to top of file, before ctor.
- Add CodeIgniter debug message to ctor.
