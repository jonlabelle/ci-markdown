CI Markdown
===========

CI Markdown is a [CodeIgniter](http://codeigniter.com) library for
parsing [Markdown](http://wikipedia.org/wiki/Markdown). It's a modified
rendition of Michel Fortin's [PHP Markdown](http://michelf.ca/projects/php-markdown/).

> **UPDATE**: [php Markdown Extra](https://michelf.ca/projects/php-markdown/extra/) now baked in!

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

The *parse()* method accepts a single parameter for a Markdown formatted
string. It returns an HTML formatted `string`.

##### Example

```php
$markdown_formatted_text = '# Heading ' . "\n\n" . '## Sub-heading' . "\n\n";
echo $this->markdown->parse($markdown_formatted_text);
// outputs <h1>Heading</h1><h2>Sub-heading</h2>
```

#### $this->markdown->parse_file();

The *parse_file()* method accepts a single parameter for a Markdown formatted
file. It returns an HTML formatted `string`.

##### Example

```php
$markdown_file_path = 'test.md';
echo $this->markdown->parse_file($markdown_file_path);
// outputs <h1>Hello world!</h1><h2>I was once in a file!</h2>
```

NOTE: If the Markdown file does not exist, `false` is returned.

Changes
-------

* See the [ChangeLog](https://github.com/jonlabelle/ci-markdown/blob/master/ChangeLog.txt) 
  for a detailed list of changes.

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
