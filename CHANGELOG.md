# Changelog

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
