# Dominic Lacaille's Resume / CV

Find the latest PDFs here:

[:page_facing_up: dominic-lacaille-cv-en.pdf](/dlacaille/resume/releases/latest/download/dominic-lacaille-cv-en.pdf)
<embed src="/dlacaille/resume/releases/latest/download/dominic-lacaille-cv-en.pdf" width="100" height="200px" />

[:page_facing_up: dominic-lacaille-cv-fr.pdf](/dlacaille/resume/releases/latest/download/dominic-lacaille-cv-fr.pdf)
<embed src="/dlacaille/resume/releases/latest/download/dominic-lacaille-cv-fr.pdf" width="100" height="200px" />

## Installing LaTeX

MacOS (Homebrew):

```sh
brew install basictex
```

Windows (Chocolatey):

```sh
choco install miktex
```

## Installing dependencies

Using `tlmgr`, install the following:

```sh
tlmgr update --self
tlmgr install classicthesis xcolor bera microtype koma-script mparhack palatino mathpazo fpl booktabs textcase titlesec tocloft footmisc caption currvita ragged2e everysel enumitem wrapfig fourier opensans fontaxes xkeyval fontawesome datenumber numprint preprint sectsty babel-french pgf
texhash
```

## Compiling the LaTeX file

```sh
pdflatex -pdf dominic-lacaille-cv-en.tex
```

## Creating a release

This repository automatically compiles a new version of the PDF files when a new version tag is pushed

```sh
git tag v1.0.0
git push --tags
```

You may also specify a release name with `-a` and `-m`

```sh
git tag -a v1.0.0 -m "Release v1.0.0"
git push --tags
```