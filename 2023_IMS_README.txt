
Information for IMS Authors Using LaTeX
----------------------------------------

1)  The file
        IMS_Paper_LaTeX_Template_Letter_V6.pdf
    contains all required format instructions for an IMS paper. Authors must 
    read this PDF file so that they understand the required format of an IMS paper.

2)  The file 
        IMS_Paper_LaTeX_Template_Letter_V6.tex
    demonstrates how to format an IMS paper correctly.

    IMS_Paper_LaTeX_Template_Letter_V6.tex has been configured to be compiled with pdfLaTeX.
    It currently uses Nimbus Roman fonts as main fonts. It has the two commands uncommented as
    shown in section 5.1 below and the two commands commented as shown in section 5.2 below.

    For more information on the requirement of main fonts for the 3 LaTeX implementations
    in TeXLive please see section 5 below.  Users of other LaTeX systems must ensure that 
    Nimbus Roman or TeX Gyre Termes or Times Roman fonts are used.

3)  Authors should make a copy of
        IMS_Paper_LaTeX_Template_Letter_V6.tex
    and then use the copy as a template by inserting their own text into the it.

    Do not reuse your past .tex files as a template, even if your past papers conformed to 
    the required format.

4)  There is no requirement to balance both columns on any page including the last page, 
    i.e. both columns are not required to be vertically aligned at the bottom. 

    As shown in the file:
    IMS_Paper_LaTeX_Template_Letter_V6.tex
    the following command must be used to prevent LaTeX from varying the vertical spacing
    to align the bottoms of both columns:
     \raggedbottom

5)  The file 
    IMS_Paper_LaTeX_Template_Letter_V6.tex has been tested with the following 3 LaTeX
    implementations in TeXLive. TeXLive is available from: http://www.tug.org/texlive/

5.1) pdfLaTeX, installed as part of TeXLive

    The Computer Modern fonts as default main fonts for pdfLaTeX must not be used.

    The Nimbus Roman fonts are based on Times Roman and are installed as part of 
    TeXLive and must be used as main fonts instead of the Computer Modern fonts.

    In order to use the Nimbus Roman fonts installed with TeXLive, authors must
    uncomment the following lines in IMS_Paper_LaTeX_Template_Letter_V6.tex:
        \usepackage{t1enc}
        \usepackage{times}

    To compile paper.tex to paper.pdf using pdfLaTeX, type the following commands:
        pdflatex paper
        bibtex paper
        pdflatex paper
        pdflatex paper

5.2) XeLaTeX, installed as part of TeXLive

    The Latin Modern Roman fonts as default main fonts for XeLaTeX must not be used.

    The TeX Gyre Termes fonts are based on Times Roman and are installed as part of
    TeXLive and must be used as main fonts instead of the Latin Modern Roman fonts.

    In order to use the TeX Gyre Termes fonts installed with TeXLive,
    authors must uncomment the following lines in IMS_Paper_LaTeX_Template_Letter_V6.tex:
        \usepackage{fontspec}% needed to change main font to TeX Gyre Termes
        \setmainfont{TeX Gyre Termes}
   
    To compile paper.tex to paper.pdf using XeLaTeX, type the following commands:
        xelatex paper
        bibtex paper
        xelatex paper
        xelatex paper

5.3) LuaLaTeX, installed as part of TeXLive

    The Latin Modern Roman fonts as default main fonts for LuaLaTeX must not be used.

    The TeX Gyre Termes fonts are based on Times Roman and are installed as part of
    TeXLive and must be used as main fonts instead of the Latin Modern Roman fonts.

    In order to use the TeX Gyre Termes fonts installed with TeXLive,
    authors must uncomment the following lines in IMS_Paper_LaTeX_Template_Letter_V6.tex:
        \usepackage{fontspec}% needed to change main font to TeX Gyre Termes
        \setmainfont{TeX Gyre Termes}

    To compile paper.tex to paper.pdf using LuaLaTeX, type the following commands:
        lualatex paper
        bibtex paper
        lualatex paper
        lualatex paper

----------------------------------------------------------

MANIFEST of this ZIP file.

1) IMS_Paper_LaTeX_Template_Letter_V6.pdf
        This PDF contains format instructions for IMS papers. 
        This PDF was created from the source file called
            IMS_Paper_LaTeX_Template_Letter_V5.tex.

2) IMS_Paper_LaTeX_Template_Letter_V6.tex
        Authors should write their papers by editing this
        source file and adding their own text.

3) The following accompanying files are included in the ZIP and are 
   required to build the sample paper IMS_Paper_LaTeX_Template_Letter_V6.pdf.

        IEEEtran.cls
            IEEE paper style file 1.8b from CTAN
            You must keep this file in the same folder as your paper .tex file.

        IEEEtran.bst
            IEEE bibliography style file
            You must keep this file in the same folder as your paper .tex file.

        IMS_modify_IEEEtran_18b_CTAN_V5.tex
            \input this file after \documentclass{IEEEtran} to change various
            settings of IEEEtran into IMS format.
            You must keep this file in the same folder as your paper .tex file.

        IEEEabrv.bib
            IEEE publication title abbreviations.
            You can discard this file if not needed.

        IEEEexample.bib
            IEEE example bibliography file
            You can insert your own bibliographic entries into this file or
            discard this file if you have your own .bib file.

        figures\*
            figure .eps files for the sample paper
            You can discard this folder.
	2023_IMS_README.txt
            this file

