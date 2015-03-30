# Changelog

## v1.3.2

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

## v1.3.1

**Release Date:** 2015-01-09

- Remove passing instance references to callbacks.

## v1.3.0

**Release Date:** 2014-12-30

- Bake in [PHP Markdown Extra](https://michelf.ca/projects/php-markdown/extra/).

## v1.2.2

**Release Date:** 2014-12-29

- Add Doc Blocks comments.

## v1.2.1

**Release Date:** 2014-12-27

- Whitespace clean-up.
- Remove legacy class constructor.

## v1.2.0

**Release Date:** 2012-10-20

- Rename `parse_markdown()` and `parse_markdown_file()` to `parse()` and `parse_file()`.
- Ensure file is readable in `parse_file()`.
- Whitespace clean-up.

## v1.1.0

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
