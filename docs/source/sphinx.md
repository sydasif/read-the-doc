# [Installing Sphinx](https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html#getting-started-with-sphinx)

Sphinx is a powerful documentation generator that has many great features for writing technical documentation including:

- Generate web pages, printable PDFs, documents for e-readers (ePub)
- You can use reStructuredText or Markdown to write documentation
- Syntax highlighted code samples

Assuming you have Python already, install Sphinx:

```console
pip install sphinx
```

Create a directory inside your project to hold your documentaion:

```console
mkdir docs
```

Run `sphinx-quickstart` in docs directory:

```console
cd docs
sphinx-quickstart
```

This quick-start will walk you through creating the basic configuration; in most cases, you can just accept the defaults. When it’s done, you’ll have an *index.rst*, *conf.py* and some other files.
