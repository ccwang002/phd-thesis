# Dissertation and Thesis Template

The is a LaTeX version of the dissertation and thesis template for The Graduate School at Washington University in St. Louis. (http://graduateschool.wustl.edu/policies-and-guides)

Template version: July 2018

## About

This document contains the guidelines for the proper formatting of dissertations and theses for doctoral and master’s degree-seeking students within the Graduate School at Washington University in St. Louis. The document is formatted using the same guidelines it describes.  Consequently, by making an extra copy of this document, you can use it as a template in which you can replace the original text with your own while still retaining the general formatting.

It is a good idea to read through this document carefully before you save it as a template and begin.  Please remember that all doctoral and master’s students are ultimately responsible for meeting the Graduate School (GS) formatting guidelines. If there is a particular issue that is not found in this template or the Dissertation/Thesis Guide, your committee or discipline should decide how it will be addressed.

Be certain to use your own full name (as recorded in [WebSTAC](https://acadinfo.wustl.edu/)) where appropriate. Make sure you use the month and year your degree is officially to be earned on the title page, abstract page and, if included, vita page(s).

Once completed, you will need to submit your document as a PDF electronically, as per the [Doctoral Dissertation Guide](http://graduateschool.wustl.edu/files/graduate/Doctoral_Dissertation_Guide.pdf) and [Master’s Thesis Guide](http://graduateschool.wustl.edu/files/graduate/Masters_Thesis_Guide.pdf), which also can be found on the Graduate School website.

## How to Use this Template

This template is a LaTeX version of The Graduate School's Microsoft Word template. To use, make a copy all of the files (or fork this repository) and start replacing the contents with your dissertation or thesis.

You will need a TeX Live installation (2020 and later) with LuaLaTeX for this template. If you use the BasicTeX distribution with only minimal packages, install the additional packages below:

    sudo tlmgr install \
        latexmk \
        biber biblatex biblatex-nature \
        csquotes \
        lualatex-math stix2-otf \
        threeparttable makecell

For your bibliography, you will need Biber installed. Please note that this template uses Biblatex (not BibTeX). Biblatex is considered a replacement for BibTeX and supports special characters and URLs in citations.

You will also need Latexmk. Latexmk compiles LaTeX documents the correct number of times. Many makefiles for LaTeX documents often compile twice. Sometimes this is unnecessary, other times it is not enough. Latexmk will correctly determine the number of compilations necessary to produce a correct document.

When including figures, please use PDF files whenever possible.

## Compiling the Document

To compile, `latexmk -lualatex thesis.tex`

To clean build files, but not the compiled document: `latexmk -C`

To clean all files, included the compiled document: `latexmk -CA`

## Differences to the Word Template

While this template fully complies with the school's style guide, there are some differences to the official word template. Please compare the compiled output at [`thesis_demo.pdf`] to the official template at [`guide/dissertation_and_thesis_template_2018.pdf`][template_pdf].

[`thesis_demo.pdf`]: https://github.com/ccwang002/wustl-latex-dissertation-template/blob/master/thesis_demo.pdf
[template_pdf]: https://github.com/ccwang002/wustl-latex-dissertation-template/blob/master/guide/dissertation_and_thesis_template_2018.pdf

Notable changes:
- No underline in chapter titles
- Header margins and font sizes are different

## Contributing

*Please help keep this template up to date with The Graduate School's Microsoft Word template.*

If you would like to submit changes to this template, please fork this repository and submit a pull request.

## License

LaTeX Project Public License version 1.3

## Change Log
Version 2021-09-12:

- Rewrite of the original `wuthesis.cls` file using memoir package

## Origin of this template
The template was rewritten by Liang-Bo Wang in 2021 based on the GitHub repo [harmsk/wustl-latex-dissertation-template]. Hence the document class was renamed from `wuthesis.cls` to `wustlthesis.cls` due to the likely incompatibility and style changes.

While it's difficult to fully trace the origins of `wuthesis.cls`, based on the file comments, Kevin Ruland created the first version of the WashU Sever Institute thesis class `wuthesis.dtx` (later converted to `wuthesis.cls`) in 1995 based on UT Austin's Thesis Style File v2 by Dinesh Das in 1995. Revisions were made by Long Duan in 1996, by Greg Hackmann in 2005, 2007, and 2008, and finally by Michael Hall, David Lu in 2014.

[harmsk/wustl-latex-dissertation-template]: https://github.com/harmsk/wustl-latex-dissertation-template/tree/f5386bb93dee6e5c0c5b1faed317b687be0f199a
