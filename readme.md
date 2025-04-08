The readme describes the usage of the preamble files used for all the documents. It doesn't particularly
describe each of the documents themselves. 

> [!Caution]
> All of the latex files are meant to be compiled in LuaLatex. They use fontspec for custom fonts, so they cannot be used using pdflatex.
> They probably work in XeLatex, though I haven't tested them.

# Dependencies

A working tex installation is needed to use the template. Aside from that, some fonts need to be installed
for using the template. All the fonts except Baskerville are free, so you can download them, if you wish.

The fonts used are listed in the table below.

| Font        | Use Case         |
|-------------|------------------|
| Baskerville | Body font        |
| [Jost](https://indestructibletype.com/Jost.html)        | Headings         |
| [Riesling](https://www.dafont.com/riesling.font)    | Heading Numbers  |


Aside from this the package `newtxmath` is used for times based math fonts. `mtp2lite` is also used for importing some symbols (in particular, 
the really nice partial symbol), so a working installation of that is needed too. To install them on linux, [this guide](https://github.com/jamespfennell/mathtime-installer) 
can be followed. We only need the lite version of the fonts which is free to use.

> [!Warning]
> For obtaining the mtpro2 lite package, head to [ctan](https://ctan.org/pkg/mtp2lite) instead of pctex's website, which was not working for me.

# Installation

First you need to clone the repo, this can be done using

```bash
git clone https://github.com/jardin-de-lys/Tex-stuff
```

Move into the directory, and the move the `layout.tex`, `environments.tex`, and `package-macros.tex` files to
wherever you wish.

Finally using the template is pretty straightforward. In your tex file, add the following to your preamble

```tex
\input{/path/to/the/files/layout.tex}
\input{/path/to/the/files/environments.tex}
\input{/path/to/the/files/package-macros.tex}
```

Replace `/path/to/the/files/` with wherever you moved the files to.

> [!Warning]
> The template is built on top of memoir, so using it with a different document class is **not possible**. The document class is already
> setup in the `layout.tex` file, so you should not use `\documentclass` command in the document, before or after inputting the prior
> code.

# Usage and Features

## Custom Commands

Some custom commands are defined for ease of access. I'll describe the most important ones. 

The command `spart` should be used instead of part. This is used for changing the margins on the part page, so that its centered (unlike the other pages).
Later, a local table of contents may also be added upon its usage.

`sidenote` acts as an alias for `marginpar`. It currently adds no extra functionality.

`chnumsep` is the length between the chapter title and the chapter number in the heading. You can adjust it per chapter by using
`\setlength{\chnumsep}{length}`, where you'd use the length in place of the `length` parameter. (For example, `10cm`).
![image](https://github.com/user-attachments/assets/e71180b9-ba81-46c4-bafc-cd26180835e1)

`incfig` is used for importing figures through inkscape, as described [here](https://castel.dev/post/lecture-notes-2/).

## Environments

To-do

## Features

To-do

# Preview

To-do
