# DOCX Find & Replace
[![Latest Version on Packagist][ico-version]][link-packagist]
[![Software License][ico-license]](LICENSE.md)
[![Latest Version on Packagist][packagist-downloads]][link-packagist]
[![Build Status](https://api.travis-ci.org/joecampo/docxfindandreplace.svg)](https://travis-ci.org/joecampo/docxfindandreplace)

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

[ico-version]: https://img.shields.io/packagist/v/campo/docxfindandreplace.svg?style=flat-square
[ico-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[link-packagist]: https://packagist.org/packages/campo/docxfindandreplace
[packagist-downloads]: https://img.shields.io/packagist/dt/campo/docxfindandreplace.svg
