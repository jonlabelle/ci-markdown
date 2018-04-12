# Codeigniter Markdown

Folk of CI Markdown, a library that parses files or text and renders html, 
a modified rendition of Michel Fortin's PHP Markdown and PHP Markdown Extra

**This library only renders the Markdown text/strings for output, for input and write to file need simple editor**

### Requirements

- php 5.2.4 or newer
- CodeIgniter 2.x or v3.x

### Install

comes included with CodeigniterPowered, but for CI 2 or CI3:

`wget https://github.com/codeigniterpower/codeigniter-markdown/blob/codeigniterpower-master/libraries/Markdown.php -O application/libraries/Markdown.php`

`wget https://github.com/codeigniterpower/codeigniter-markdown/blob/codeigniterpower-master/config/markdown.php -O application/config/markdown.php`

# Using the Markdown Class

In controlers or in the views.

### Configuration

Customized [PHP Markdown settings (click for reference)](https://michelf.ca/projects/php-markdown/configuration/)
can be specified in the `config/markdown.php` config file.

### Initializing the Class

In your controller using the `$this->load->library()` method:

```php
$this->load->library('markdown');
```

Once loaded, the Markdown library object will be available using:

```php
$this->markdown
```

### Examples

#### Markdown Text to HTML

- `$this->markdown->parse()`

Accepts a single `string` parameter of Markdown *text* and returns the parsed
HTML.

```php
$this->load->library('markdown');

$markdownText = "# Heading "."\n\n"."## Sub-heading"."\n\n";
echo $this->markdown->parse($markdownText);
>>> <h1>Heading</h1><h2>Sub-heading</h2>
```

#### Markdown File to HTML

- `$this->markdown->parse_file()`

Accepts a single `string` parameter for a Markdown *file path* and returns the
parsed HTML.

```php
$this->load->library('markdown');

echo $this->markdown->parse_file('/path/to/markdown/file.md');
>>> <h1>CI Markdown</h1><p>CI Markdown is a modified rendition...</p>
```

## Issues

This is specific AD-HOC folk for Codeigniter-powered, see original project for.

https://github.com/jonlabelle/ci-markdown/issues/new

## Credits

- John Gruber: http://daringfireball.net/
- Michel Fortin: https://michelf.ca/home/

## Author

- Jon LaBelle <contact@jonlabelle.com>

