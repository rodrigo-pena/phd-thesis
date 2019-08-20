# `latex/`

## About

The files in this directory contain the $\LaTeX$ code needed to compile the `.pdf` file of the thesis.



## Reproducibility

To properly compile the `.pdf` file, you should install an up-to-date $\LaTeX$ distribution to you system. Then, open a terminal window, navigate to the `phd-thesis/latex/` folder and type the following commands, in order:

```bash
pdflatex my_thesis.tex
bibtex my_thesis.tex
pdflatex my_thesis.tex
pdflatex my_thesis.tex
makeglossaries my_thesis.tex
makeindex my_thesis.tex
pdflatex my_thesis.tex
bibtex my_thesis.tex
pdflatex my_thesis.tex
pdflatex my_thesis.tex
```

Alternatively, you could configure your favorite $\LaTeX$ editor to run these commands as a custom build procedure.

In the end, the re-compiled thesis will be available in the `my_thesis.pdf` file.



## Folder structure

- `head/`
  - All the text before the first chapter (abstracts, acknowledgements, etc.).
- `images/`
  - All the images used in the thesis.
- `main/`
  - All the chapters forming the main text of the thesis.
- `settings/`
  - Configuration code relating to typesetting customization.
- `tail/`
  - All the text after the last chapter (bibliography, cv, etc.).
- `utopia_font/`
  - Typesetting files for the [Utopia][utopia] typeface.



## Acknowledgements

This folder started from an unoffical [EPFL thesis template][epfl-template] maintained by [PolyDoc][polydoc].



[epfl-template]: https://github.com/glederrey/EPFL_thesis_template
[polydoc]: https://polydoc.epfl.ch/
[utopia]: https://en.wikipedia.org/wiki/Utopia_(typeface)