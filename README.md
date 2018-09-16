# Codeigniter - Markdown

Powered rendering libray that parses files of text and renders html output for codeigniter.

It's convert the static contents of a text files (like thist) and will output a formatted html web page, of any markdown text file or markdown string parameter. Of course, its not an editor, its the utillity that take the contents and renders as html.
Tis its a folk of CI Markdown, a library that parses files or text and renders html, 
a modified rendition of Michel Fortin's PHP Markdown and PHP Markdown Extra

## FEATURES

*  **Simple mardkdown rendering helper/class**. to get string and out that as html page.

## INSTALLING

Comes included with CodeigniterPowered, but for CI 2 or CI3:

**Requirements**

* Codeigniter 2.x or 3.x

**Manual controlled install**

**1)** Located your Codeigniter proyect and then download the repository at the `Applications` root directory

`wget https://github.com/codeigniterpower/codeigniter-markdown/blob/codeigniterpower-master/libraries/Markdown.php -O libraries/Markdown.php`

`wget https://github.com/codeigniterpower/codeigniter-markdown/blob/codeigniterpower-master/config/markdown.php -O config/markdown.php`

**2)** The contents must be two files at that places:

* `config/markdown.php` 
* `libraries/Markdown.php`

**3)** Then, just In controlers or in the views:
    
``` php
$this->load->library('markdown');
echo $this->markdown->parse("# title "."\n\n"."normal text: hello world"."\n\n");
```

Now the output wil renders a "H1" tag title and some text.


## CONFIGURATION

Wil be located at the `config/markdown.php` file, and heres the documentation: https://michelf.ca/projects/php-markdown/configuration/#markdown .

## USAGE

**As simple as load and parse text** On each request and response, at controllers or views:

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

## Credits

This is specific AD-HOC folk for Codeigniter-powered, see original project for.

- Jon LaBelle <contact@jonlabelle.com>

https://github.com/jonlabelle/ci-markdown/issues/new
