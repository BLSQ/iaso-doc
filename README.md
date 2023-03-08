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
![Screenshot 2022-06-28 at 10 50 11](https://user-images.githubusercontent.com/38907762/223693392-7a6b9f07-b4be-41ff-8ff6-45783ac41d52.png)

### Convert a docx file to md

- Install [pandocs](https://pandoc.org/installing.html)
- Add the file you want to convert to `/docs/originals`
- cd to `/docs`
- Run `pandoc -s -f docx -t markdown_mmd --extract-media=. -o ./<filename>/<filename>.md ./originals/<original_filename>.docx`
- The command creates a `/media` folder in `/docs`: move it to `/docs/<filename>`. Now you should have a folder: `/docs/<filename>/media`. This moving around is due to the way pandoc create the path to the files when converting and to the way mkdocs alters the paths when building
- Add an entry in `mkdocs.yml`. Follow the current convention
