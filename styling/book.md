# Extend website and ebook style

You can extend css used in the ebooks and the website by creating files in the `styles` directory:

| Type | File |
| ---- | ---- |
| `website` | `styles/website.css` |
| `pdf` | `styles/pdf.css` |
| `epub` | `styles/epub.css` |
| `mobi` | `styles/mobi.css` |
| `pdf`, `epub`, `mobi` | `styles/ebook.css` |


These paths can be changed in the `book.json` configuration, for example to use file in the root folder:

```json
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

#### Using a CSS pre-processor

There are plugins that make it easy to use a CSS pre-processor:

- [styles-less](https://plugins.gitbook.com/plugin/styles-less)
- [styles-sass](https://plugins.gitbook.com/plugin/styles-sass)

