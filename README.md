# My PhD Thesis

If you want to use the same thesis template or want to build on top of it, please check out my fork of the WUSTL dissertation and thesis template at <https://github.com/ccwang002/wustl-latex-dissertation-template>. It also comes with [an example][thesis-template-example] using the template.

[thesis-template-example]: https://raw.githubusercontent.com/ccwang002/wustl-latex-dissertation-template/master/thesis_demo.pdf


## Instructions to build the document
Use LuaLaTex on Tex Live 2020 and later. For the BasicTeX distribution on macOS, install the additional packages below:

    sudo tlmgr install \
        latexmk \
        biber biblatex biblatex-nature \
        lualatex-math stix2-otf \
        csquotes threeparttable multirow \
        enumitem siunitx

Build the document by:

    latexmk -lualatex thesis.tex

Clean up intermediate files by:

    latexmk -c
    latexmk -C  # also remove the built PDF
