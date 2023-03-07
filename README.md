## IASO-DOC

**Under construction**

Documentation for Iaso users buld with [mkdocs](https://www.mkdocs.org) and aimed to be deplyed on [readthedocs](https://readthedocs.org/).

The goal is to provide documentation that is easy to access for users, and (reasonably) easy to edit for non-technical users. There's a clear inspiration from [openIMIS docs](https://docs.openimis.org/en/latest/)

### Targeted features
Outside of readthedocs core features:

- [ ] Setup the project so that the structure (tree) of the documentation can be easily modified
- [ ] Provide a convenient way to convert existing documentation (mostly `.docx` files) to markdown

### How to test

You need Python > 3.8.

- clone the repo
- cd to `/docs`
- `pip install -r requirements.txt`
- `mkdocks serve`
