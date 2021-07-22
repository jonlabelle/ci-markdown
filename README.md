# CI Markdown

CI Markdown is a modified rendition of Michel Fortin's [PHP Markdown][1]
and [PHP Markdown Extra][2] for [CodeIgniter][3].

## Install

### Requirements

- [PHP][4] version 5.4.8 or newer
- [CodeIgniter][3] version 2.x – v3.x

### Download

Download and extract the [zip][5] release to your CoddeIgniter
`application/libraries/` directory.

**The extracted path should resemble:**

- `application/libraries/Markdown.php`

## Usage

### Configuration

Custom [PHP Markdown settings](https://michelf.ca/projects/php-markdown/configuration/)
are defined in the [config/markdown.php](config/markdown.php) config file.

### Initializing the Markdown Class

Like most other classes in CodeIgniter, initialize it from your controller
using the `$this->load->library()` method:

```php
$this->load->library('markdown');
```

To programmatically configure the Markdown instance, overriding any matched
settings defined in the [config file](config/markdown.php):

```php
$config = array(
    'tab_width' => 2,
    'no_markup' => true,
    'empty_element_suffix' => '/>'
);

$this->load->library('markdown', $config);
```

#### Markdown to HTML

- `$this->markdown->transform()`

Accepts a single `string` parameter of Markdown *text* and returns the
transformed HTML.

```php
$this->load->library('markdown');

$markdownText = "# Heading "."\n"."## Sub-heading";
echo $this->markdown->transform($markdownText);
// <h1>Heading</h1>
// <h2>Sub-heading</h2>
```

#### Markdown file to HTML

- `$this->markdown->transform_file()`

Accepts a single `string` parameter for a Markdown *file path* and returns the
transformed HTML.

```php
$this->load->library('markdown');

echo $this->markdown->transform_file('/path/to/markdown/file.md');
// <h1>Heading</h1>
// <h2>Sub-heading</h2>
```

## Issues

For all issues including feature requests, please [open a new issue][6].

## Changes

See the [Changelog][7] page.

## Credits

- [John Gruber](http://daringfireball.net/)
- [Michel Fortin](https://michelf.ca/home/)

[1]: https://michelf.ca/projects/php-markdown/
[2]: https://michelf.ca/projects/php-markdown/extra/
[3]: https://www.codeigniter.com
[4]: https://php.net
[5]: https://github.com/jonlabelle/ci-markdown/archive/master.zip
[6]: https://github.com/jonlabelle/ci-markdown/issues/new
[7]: https://github.com/jonlabelle/ci-markdown/blob/master/CHANGELOG.md
