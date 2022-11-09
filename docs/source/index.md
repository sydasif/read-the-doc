% Docs Notebook documentation master file, created by
% sphinx-quickstart on Wed Nov  9 10:13:01 2022.
% You can adapt this file completely to your liking, but it should at least
% contain the root `toctree` directive.

```{include} ../../README.md
:relative-images:
```

See my {doc}`link/my-conf-file`.

See my {ref}`Index file` for refrence.

```{warning}
This is a test project to create documentaion.
```

```{toctree}
:caption: 'Table of Contents:'
:maxdepth: 2

Installing Sphinx <sphinx>
Markdown with Sphinx <markdown>
Index file <link/my-index-file>
Configuration file <link/my-conf-file>
```
