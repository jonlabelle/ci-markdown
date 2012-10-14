CI Markdown
===========

CI Markdown is a [CodeIgniter](http://codeigniter.com) library for parsing [Markdown](http://wikipedia.org/wiki/Markdown) formatted text in CodeIgniter. It is a modified version of Michel Fortin's [PHP Markdown](http://michelf.ca/projects/php-markdown/).

**Modifications include:**

- *Markdown_Parser* class renamed to *Markdown*
- Removed WordPress interface.
- Removed Smarty interface.
- Removed Textile interface.
- Removed BBLOG interface.
- The `Markdown()` function is now an instance method, and marked *deprecated*.
- Changed default empty element suffix to produce HTML-style tags (`>`).
- Changed default tab width to *2*.
- Changed class constructor to PHP5 style constructor.
- *Private* class members are declared `private` instead of `var`.
- Removed all constant definitions and references.
- All *private* class members are at the top, before the constructor.
- Add log message on class initialization (debug) .
- Added `$_ci` member for CodeIgniter super object reference.
- Only expose Markdown parsing methods, `parse_markdown()` and `parse_markdown_file`.

Requirements
------------

- PHP 5.2x+
- CodeIgniter v2.1.0 to v3.x-dev

Installation
------------

Save `Markdown.php` to your CodeIgniter `application/libraries` folder.

Usage
-----

### Loading

Load the CI Markdown library from your *Controller* class.

```php
$this->load->library('markdown');
```

Or auto-load it from your `application/config/autoload.php` file.

```php
$autoload['libraries'] = array('markdown');
```

### Parsing Markdown

There are <em>two</em> methods for parsing Markdown formatted content.

##### $this->markdown->parse_markdown()

`parse_markdown()` accepts a single string parameter for Markdown formatted text. It parses and returns the input as an HTML formatted string.

```php
$this->markdown->parse_markdown($markdown_text);
```

##### $this->markdown->parse_markdown_file();

`parse_markdown_file()` also accepts a single parameter which should be a <em>valid</em> Markdown file path. This method reads the contents of the Markdown file and returns them as an HTML formatted string.

```php
$this->markdown->parse_markdown_file($file_path);
```

NOTE: If the file does not exist, `false` will be returned.

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