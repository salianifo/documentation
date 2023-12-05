# Dialogic 2 - Documentation Repository

This repository contains the documentation of Dialogic 2.

It utilises [mdBook](https://rust-lang.github.io/mdBook) to generate and render the website.
If you find a mistake, please open an issue.

## Adding a new page
New pages should be added to the `documentation` folder. The `SUMMARY.md` file contains the table of contents displayed as a sidebar. Please add your new page to this file.

## Updating the website
The `md` files can be displayed in many applications supporting markdown. However, the website is generated using `mdBook`. The website utilises a build script to generate the website and push it to the `gh-pages` branch. On GitHub, these build scripts are called GitHub Actions.

## Book Structure
The `documentation` folder contains the book pages.

The `theme` folder overrides the [built-in](https://github.com/rust-lang/mdBook/tree/master/src/theme) `mdBook` files. 

The `book-toml` contains the configuration of the documentation book.

A preprocessor decides how the book's chapters will be modified before building the final published book.\
The preprocessors are not part of the built-in feature set and were developed by other developers.\
They must be installed, see the [`.github/workflows/mdbook.yml`](https://github.com/dialogic-godot/documentation/blob/main/.github/workflows/mdbook.yml) for this.

## Admonish
The documentation supports admonish. We use a preprocessor for this.
You can create these by using the following syntax, using `info` as an example category:
````
```admonish info
The info text goes here.
```
````

Some available admonish categories: `info`, `warning`, `danger`, `tip`, `question`, `bug`, `example`, …

All admonish categories: https://tommilligan.github.io/mdbook-admonish/reference.html#directivese
