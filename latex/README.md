# `latex/`

This directory contain the $\LaTeX$ code needed to compile the `.pdf` file of the thesis.


## Reproducibility

Make sure that you have an up-to-date $\LaTeX$ distribution in your system. Then, open a terminal window, navigate to the `phd-thesis/latex/` folder and type the following commands, in order:

```bash
pdflatex my_thesis.tex
bibtex my_thesis.tex
pdflatex my_thesis.tex
pdflatex my_thesis.tex
makeglossaries my_thesis.tex
pdflatex my_thesis.tex
bibtex my_thesis.tex
pdflatex my_thesis.tex
pdflatex my_thesis.tex
```

Alternatively, you could configure your favorite $\LaTeX$ editor to run these commands as a custom build procedure. In the end, the re-compiled thesis will be available in the `my_thesis.pdf` file.


## Folder structure

- `head/`
  - Contains all the text coming before the first chapter (abstracts, acknowledgements, etc.).
- `images/`
  - Contains all the images used in the thesis.
- `main/`
  - Contains all the chapters forming the main text of the thesis.
- `settings/`
  - Contains configurations regarding typesetting customization.
- `tail/`
  - Contains all the text after the last chapter (bibliography, cv, etc.).
- `utopia_font/`
  - Contains the typesetting files for the [Utopia][utopia] typeface.


## Acknowledgements

This folder started from an unoffical [EPFL thesis template][epfl-template] maintained by [PolyDoc][polydoc].


[epfl-template]: https://github.com/glederrey/EPFL_thesis_template
[polydoc]: https://polydoc.epfl.ch/
[utopia]: https://en.wikipedia.org/wiki/Utopia_(typeface)
