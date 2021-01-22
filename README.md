# Electron Cash Documentation

This is a set of notes for writing the documentation for Electron Cash.

The documentation is written using the (Sphinx Python Documentation Generator)[http://www.sphinx-doc.org/en/stable/].

# Generating Documentation
Make sure sphinx is installed with `pip install sphinx`.

You can generate the documentation locally, from the root directory of this project, using 
`make html`. The documentation will be produced in the `_build/html` directory, in HTML format.


# Updating Documentation Versions
When the documentation is updated, the version number needs to be updated in the following places:

* conf.py - lines 58 & 60
