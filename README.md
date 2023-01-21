# paperaj-template - Write jounal papers or thesis in word and convert to LaTeX for submission! (All using GitHub actions!)

TL;DR: *You can use any LaTeX template! Sections in the word document ([see main.docx](main.docx)) with italicized headings are split into latex files that can be included into your template*
See example in [main.tex](main.tex) and [inclusions.tex](inclusions.tex)

## This is a template that uses [paperaj](https://github.com/dermatologist/paperaj) as a GitHub action.

Paperaj is a combination of bash and python scripts for converting MS word document to a latex document for academic journals. You can use any journal template for latex compilation. This can be used as a standalone script (needs pandoc and latex installed) or as a GitHub action. **Just create a repo from this template that uses [Paperaj](https://github.com/dermatologist/paperaj) GitHub action and the GitHub will latex-compile your manuscript!**

[![paperaj](https://github.com/dermatologist/paperaj/blob/develop/paperaj.drawio.svg)](https://github.com/dermatologist/paperaj/blob/develop/paperaj.drawio.svg)

## How it works
Paperaj creates a set of plain latex files from the word document in the paperaj folder. Images, tables and referencing are supported during the conversion. These plain latex files can be included in the journal's latex template using: ``` \input{filename} ```. See [main.docx](https://github.com/dermatologist/paperaj-public-template/blob/master/main.docx) in the template for word document format. See [main.tex](https://github.com/dermatologist/paperaj-public-template/blob/master/main.tex) in the template to see how you can include paperaj generated latex files in the latex entry file. Just use this template that uses [Paperaj GitHub action](https://github.com/dermatologist/paperaj) and the **GitHub will latex-compile your manuscript!**

## Usage

### As GitHub action (recommended)
* Use this [github template](https://github.com/dermatologist/paperaj-public-template)
* Use the docx in the template
* Add bib and tex files.
* set the names of docx, bib and latex entry in paperaj.env file
* This template generates LaTeX files on push to develop branch and compile to PDF on push to main branch!


### Arguments in .env file (Needed only if compiling locally)

* BIBLIO=references.bib
* DOCX=article.docx
* PDF=article.pdf
* LATEXFOLDER=./ # no trailing /
* LATEXENTRY=main.tex
* BIBCOMPILE=bibtex or biber
* TEXCOMPILE=defer or yes
* ACRONYMS=sample.csv
* GLOSSARY=sample.csv
* MINDMAP=create
* CITETAG= cite or citep
* PANDOCPATH=

### Figures

* Use TWO_COLUMN or LATEXROTATE in captions of figure
* FIGURE_ or TABLE_ for inline ref

### Referencing

\cite{AuthorYEAR} inline

#### Using Zotero

* [Use this csl](word2latex-pandoc.csl)

### Flatten into single latex file without inclusions

* Just create a folder called **flatten**.

### arXiv

* Add required latex files to **arxiv** folder.

### Clean version for submission

* The clean latex files without latex comments for submission is in the **clean** folder.

### Mindmapping

#### [plant UML](https://github.com/plantuml/plantuml/releases/download/v1.2022.14/plantuml-1.2022.14.jar)

* '** first'
* '*** second'
* '**_' adds title

* Add the above to the Zotero notes for references

### Notebook to pdf
* jupyter-nbconvert --to pdf acnode.ipynb

### Extract highlights from PDF
[pdfannots](https://pypi.org/project/pdfannots/)

## Other Instructions:

* set repo permissions to read/write
* set entry.tex as overleaf entry


## Give us a star ⭐️
If you find this project useful, give us a star. It helps others discover the project.
## Contributors

* [Bell Eapen](https://nuchange.ca) | [![Twitter Follow](https://img.shields.io/twitter/follow/beapen?style=social)](https://twitter.com/beapen)