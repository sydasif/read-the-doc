# Markdown with Sphinx

You can use *Markdown using MyST* Sphinx project.

## [RST-to-MyST](https://rst-to-myst.readthedocs.io/en/latest/)

A tool for converting ReStructuredText to MyST Markdown. We will convert *.rst* file into *.md* extension.

To install from PyPI:

```console
pip install "rst-to-myst[sphinx]"
```

To then run a basic conversion of a whole project:

```console
rst2myst convert docs/**/*.rst
```

The above command has convert the index.rst into index.md, now delete index.rst from your poject.

## [Myst-Parser](https://myst-parser.readthedocs.io/en/latest/intro.html)

This page describes how to get started with the MyST parser, with a focus on enabling it in the Sphinx documentation engine.

To install use pip:

```console
pip install myst-parser
```

To use the MyST parser in Sphinx, simply add the following to your *conf.py* file:

```py
extensions = ["myst_parser"]
```

This will activate the MyST Parser extension, causing all documents with the *.md* extension to be parsed as MyST.

Now, edit your *index.md* and add some information about your project. 

```console
    % ansible notebook documentation master file, created by
    % sphinx-quickstart on Wed Nov  9 10:13:01 2022.
    % You can adapt this file completely to your liking, but it should at least
    % contain the root `toctree` directive.

    ```{include} ../../README.md
    :relative-images:
    ```

    ```{warning}
    This is a test repo for learning
    ```

    ```{toctree}
    :caption: 'Contents:'
    :maxdepth: 2
    ```
```

Build them to see how they look:

```console
make html
```

Your index.md has been built into index.html in your documentation output directory. Open index.html (build/html/index.html) file in your web browser to see your docs.
