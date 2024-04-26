This style allows to use the dinat style from the natbib latex package in English, so using "and" and "et al" instead of "und" and "u. a.".

You need to have installed the natbib package as well as have `\usepackage{natbib}` in your preamble and use style `dinat`. Then replace the `dinat.bst` on your computer with the one in this repository.
You can find the file with `kpsewhich dinat.bst`.

More info:
https://tex.stackexchange.com/questions/450579/et-al-extension-using-dinat-natbib-style

I'd also recommend adding
```
%removes the brackets/paranthesis around the year
\setcitestyle{open=,close=}

%renames cite to oldcite
\let\oldcite\cite
%define our own cite command that includes brackets
\renewcommand{\cite}[1]{[\oldcite{#1}]}
```
to your preamble.
