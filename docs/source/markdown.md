# Markdown with Sphinx

You can use *Markdown using MyST* in the Sphinx project.

## [RST-to-MyST](https://rst-to-myst.readthedocs.io/en/latest/)

A tool for converting ReStructuredText to MyST Markdown. this tool convert the *.rst* file into *.md* extension.

To install from PyPI:

```console
pip install "rst-to-myst[sphinx]"
```

Basic conversion command of a whole project:

```console
rst2myst convert docs/**/*.rst
```

The above command has converted the index.rst into an index.md, now delete index.rst from your project.

## [Myst-Parser](https://myst-parser.readthedocs.io/en/latest/intro.html)

To get started with the MyST parser, with a focus on enabling it in the Sphinx documentation engine.

To install use pip:

```console
pip install myst-parser
```

To use the MyST parser in Sphinx, simply add the following to your *conf.py* file:

```py
extensions = ["myst_parser"]
```

This will activate the MyST Parser extension, causing all documents with the *.md* extension to be parsed as MyST.

Now, edit your *index.md* file and add some information about your project.

Add below line to include README.md file:

```console
    ```{include} ../../README.md
    :relative-images:
    ```
```

Add warning for project:

```console
    ```{warning}
    This is a test project.
    ```
```

Update your toctree:

```console
    ```{toctree}
    :caption: 'Table of Contents:'
    :maxdepth: 2

    Installing Sphinx <sphinx>
    Markdown with Sphinx <markdown>
    Index file <link/my-index-file>
    Configuration file <link/my-conf-file>
    ```
```

Add ref/link as below:

```console
    ```{include} ../../README.md
    :relative-images:
    ```

    See my {doc}`link/my-conf-file`.

    See my {ref}`Index file` for refrence.

    ```{warning}
    This is a test project to create documentaion.
    ```
```

Build them to see how they look:

```console
make html
```

Your index.md has been built into index.html in your documentation output directory (build/html/index.html). Open the index.html file in your web browser to see your docs.
