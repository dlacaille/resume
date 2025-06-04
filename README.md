# Dominic Lacaille's Resume / CV

Find the latest PDFs here:

[:page_facing_up:dominic-lacaille-cv-en.pdf](https://github.com/dlacaille/resume/releases/latest/download/dominic-lacaille-cv-en.pdf)

[:page_facing_up:dominic-lacaille-cv-fr.pdf](https://github.com/dlacaille/resume/releases/latest/download/dominic-lacaille-cv-fr.pdf)

## Why?

Why not! Using a declarative language like Latex for my resume allows me to comment out experience to tailor my CV. I also love the idea of using a declarative language for typesetting, where I don't have to fight with Word for alignment or spacing.

Here's a list of other reasons for using Latex:
- Declarative is better than WYSIWYG
- Beautiful, the typesetting of Latex is unmatched
- Can add comments
- Don't need a specific version of Word to get my resume to look the way I want
- Build it with CI!
- The challenge is fun and rewarding

## Installing LaTeX

MacOS (Homebrew):

```sh
brew install basictex
```

Windows (Chocolatey):

```sh
choco install texlive
```

## Installing dependencies

Using `tlmgr`, install the following:

```sh
tlmgr update --self
tlmgr install latexmk classicthesis xcolor bera microtype koma-script mparhack palatino mathpazo fpl booktabs textcase titlesec tocloft footmisc caption currvita ragged2e everysel enumitem wrapfig fourier opensans fontaxes xkeyval fontawesome5 datenumber numprint preprint sectsty babel-french pgf
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
