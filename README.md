CI Markdown
===========

CI Markdown is a [CodeIgniter](http://codeigniter.com) library for parsing [Markdown](http://wikipedia.org/wiki/Markdown). It's a modified rendition of Michel Fortin's [PHP Markdown](http://michelf.ca/projects/php-markdown/).

See the [ChangeLog](https://github.com/jonlabelle/ci-markdown/blob/master/ChangeLog.txt) for a complete list of *PHP Markdown* modifications.

Requirements
------------

- PHP 5.2x+
- CodeIgniter v2.1.0 to v3.x-dev

Installation
------------

Save `Markdown.php` to your CodeIgniter `application/libraries` folder.

Usage
-----

### Loading the Library

Load the CI Markdown library from your *Controller*.

```php
$this->load->library('markdown');
```

Or auto-load it from your `application/config/autoload.php` config file.

```php
$autoload['libraries'] = array('markdown');
```

### Parsing Markdown

#### $this->markdown->parse()

```php
$markdown_formatted_text = '# Heading' . "\n" . '## Sub-heading';
echo $this->markdown->parse($markdown_formatted_text);
```

`parse_markdown()` accepts a single `string` parameter of the Markdown formatted text. It parses and returns the Markdown as an HTML formatted `string`.

#### $this->markdown->parse_file();

```php
$markdown_file_path = 'test.md';
echo $this->markdown->parse_file($markdown_file_path);
```

`parse_file()` also accepts a single `string` parameter of a Markdown file path. It parses and returns the Markdown as an HTML formatted `string`.

NOTE: If the Markdown file does not exist, `false` will be returned instead of `string`.

Changes
-------

* See the [ChangeLog](https://github.com/jonlabelle/ci-markdown/blob/master/ChangeLog.txt).

TODO
----

- Unit tests

Resources
---------

* [PHP Markdown](http://michelf.ca/projects/php-markdown/)
* [Markdown](http://daringfireball.net/projects/markdown/)

Feedback
--------

Jon LaBelle
<contact@jonlabelle.com>

Issues
------
<https://github.com/jonlabelle/ci-markdown/issues>