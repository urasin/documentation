# Configuration

All configurations are stored as JSON in a file named `book.json`.

You can paste your `book.json` at [jsonlint.com](http://jsonlint.com) to validate the JSON syntax.

All fields are optionals or default to some extracted values.


## Fields

#### gitbook

```js
{ "gitbook": "2.x.x" }
```

This option is used to detect which version of GitBook will be use to generate the book.
The format is a [SEMVER](http://semver.org) condition.

#### title

```js
{ "title": "My Awesome Book" }
```

This option defines the title of your book, by default this value is extracted from the **README** (first title).

On **gitbook.com**, this value is defined from the title entered on the platform.

#### description

```js
{ "description": "This is such a great book!" }
```

This option defines the description of your book, by default this value is extracted from the **README** (first paragraph).

On **gitbook.com**, this value is defined from the description entered on the platform.

#### isbn

```js
{ "isbn": "978-3-16-148410-0" }
```

This option defines the ISBN associated with your book 

#### language

```js
{ "language": "fr" }
```

This option defines the language of your book, by default value is `en`.

This option is used for internationalization and localization, it changes the text from the website.

On **gitbook.com**, this value is defined from the language detected in the content or specified in the settings.

#### direction

```js
{ "direction": "rtl" }
```

This option is used to override the text direction from the language.
It is recommended to set the `language` field to a language with the correct text direction instead.

#### styles

This option is used to add custom css to your book.

Example:

```js
{
    "styles": {
        "website": "styles/website.css",
        "ebook": "styles/ebook.css",
        "pdf": "styles/pdf.css",
        "mobi": "styles/mobi.css",
        "epub": "styles/epub.css"
    }
}
```

#### plugins

```js
{ "plugins": ["mathjax"] }
```

The list of plugins being used by a book is defined in the `book.json` configuration.

#### pluginsConfig

```js
{
    "plugins": ["myplugin"],
    "pluginsConfig": {
        "myPlugin": {
            "message": "Hello World"
        }
    }
}
```

This option contains all plugins specific configurations.

#### structure

This option is used to override files paths used by GitBook.

For example if you want to use `INTRO.md` instead of `README.md`:

```js
{
    "structure": {
        "readme": "INTRO.md"
    }
}
```

Structure types are `readme`, `langs`, `summary` and `glossary`.

#### variables

```js
{
    "variables": {
        "myTest": "Hello World"
    }
}
```

This option defines the variables values being used in [templating](./templating.md).

#### pdf

PDF specific options allow customization of header, footer, etc

```js
{
    "pdf": {
        "headerTemplate": "Header of the PDF with _TITLE_",
        "footerTemplate": "Footer HTML template. Available variables: _PAGENUM_, _TITLE_, _AUTHOR_ and _SECTION_."
    }
}
```
