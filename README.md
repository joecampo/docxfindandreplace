# DOCX Find & Replace
This is a simple find and replace utility for DOCX files. Simple way to take a DOCX template, map some variables, and save a new copy.

## Installation

Via Composer

``` bash
$ composer require campo/docxfindandreplace
```

## Usage
In your DOCX template you will need to wrap any variables you would like to replace with curly braces (e.g. ``{FIRSTNAME}``. Be sure to use variables in your template that are all **uppercase** as Microsoft Word's spell check will create issues. 
``` php
\Campo\DocxFindAndReplace\Docx::create(__DIR__ . "/template.docx")->replace(
    [
        'FIRSTNAME' => 'Joe',
        'LASTNAME' => 'Campo',
    ]
)->save(__DIR__ . '/newfile.docx');
```
## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.