# My PhD Thesis

## Instructions to build the document
Use LuaLaTex on Tex Live 2020 and later. For the BasicTeX distribution on macOS, install the additional packages below:

    sudo tlmgr install \
        latexmk \
        biber biblatex biblatex-nature \
        lualatex-math \
        csquotes threeparttable siunitx

Build the document by:

    latexmk -lualatex thesis.tex

Clean up intermediate files by:

    latexmk -c
    latexmk -C  # also remove the built PDF
