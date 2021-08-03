---
layout: "layout"
title:  "eBook with LaTeX"
permalink: /LaTeX04/
---

* [Downloard TARBALL](../tarballs/LaTeX04.tar.bz2)
* [PDF](JennyWren.pdf)

<br>
### JennyWren.tex

```
{% raw %}
\newcommand{\rev}{01 - 23-Jul-2021}
% REV01 Fri 23 Jul 2021 16:51:45 WIB
% START Fri 26 Mar 2021 12:10:02 WIB

\documentclass[12pt]{book}
\usepackage[a4paper, margin=50pt]{geometry}
\usepackage[dvipsnames,table,xcdraw]{xcolor}
\usepackage{colortbl}
\usepackage[hidelinks]{hyperref}
\usepackage[pdftex]{graphicx}
\definecolor{links}{HTML}{0011FF}
\hypersetup{colorlinks,linkcolor=,urlcolor=links}

% Should be loaded after the hyperref and bookmark packages
\usepackage{chngcntr}
\counterwithin*{chapter}{part}
% \counterwithout{chapter}{part}

\newcommand{\pengarangs}{%
    Dickens McCartney\\
}
\newcommand{\judul}{%
Jenny Wren\\[13pt]
Our Mutual Friend
}

\begin{document}

\begin{titlepage}
    \begin{center}    

    \vspace*{15mm}
    \textbf{\Large \judul}

    \vspace*{30mm}       
    \textbf{by}

    \vspace*{15mm}    
    \textbf{\Large \pengarangs}

    \vspace*{4.0cm}

    \begin{center}
        \includegraphics[width=40mm]{ucls-coat}
    \end{center}

    \textbf{
       Universe Centra Le Sahara (UCLS)\\[10pt]
       Omar Bakry School of Management\\[10pt]
       Jabal Acacus Campus, Ghat. \\[10pt]
       \url{https://jennywren.vlsm.org/} \\[10pt]
       Rev. \rev%
    }

    %\vspace*{5mm}    
    %\textbf{\LARGE \textcolor{red}{***** Work In Progress *****}}

    \end{center}

\end{titlepage}

\pagenumbering{roman}

\tableofcontents

\newpage

\chapter*{Jenny Wren}
\addcontentsline{toc}{chapter}{Jenny Wren}

\begin{verbatim}
Like so many girls
Jenny Wren could sing
But a broken heart
Took her soul away

--- Dickens McCartney
\end{verbatim}

\noindent
Jenny Wren lyrics \copyright MPL Communications Ltd. See also \url{https://jennywren.vlsm.org/}.
\\[1pt]

\noindent
Jenny Wren --- whose real name is Fanny Cleaver,
is ''the dolls' dressmaker'' with whom Lizzie lives after her father dies.
She is crippled with a bad back, although not ugly.
She is very motherly towards her drunken father, whom she calls her ''bad child''.
Jenny later cares for Eugene while he recovers from Headstone's attack on his life.
She may have a romance with Sloppy at the end of the book,
which the reader may surmise will end in marriage.
Although her mannerisms give her a certain ''strangeness'', Jenny is very perceptive,
identifying Eugene Wrayburn's intentions towards Lizzie in his small actions.
Her role is a creator and a caretaker, 
and her ''pleasant fancies'' of ''flowers, bird song, numbers of blessed, 
white-clad children'' reflect the mind's ability to rise above adverse 
circumstances --- \url{https://en.wikipedia.org/wiki/Jenny_Wren}
\\[1pt]

\noindent
Jenny Wren aka Fanny Cleaver --- Sharp and sassy maker of doll's clothes, 
pincushions, and pen-wipers. 
Crippled (my back’s bad, and my legs are queer),
she lives with her drunken father whom she refers to as her bad child.
Lizzie Hexam, after the death of her father,
takes lodging with Jenny who helps Lizzie escape London when pursued by Bradley Headstone and Eugene Wrayburn.
It was difficult to guess the age of this strange creature,
for her poor figure furnished no clue to it,
and her face was at once so young and so old. Twelve,
or at the most thirteen, might be near the mark --- 
\url{https://www.charlesdickenspage.com/dickens-characters-t-z.html}
\\[1pt]

\noindent
=== Rev. \rev ===

\newpage

\pagenumbering{arabic}

\part{Book the First:\\THE CUP AND THE LIP}
\input{01-01.tex}
\part{Book The Second:\\BIRDS OF A FEATHER}
\input{02-01.tex}
\part{Book The Third:\\A LONG LANE}
\input{03-01.tex}
\part{Book The Fourth:\\A TURNING}
\input{04-01.tex}
\part{Take Note!}
\input{Full-License.tex}

% %%%%%%%%%%%%%%%%
\end{document}%%%%
% End of document.
% %%%%%%%%%%%%%%%%

{% endraw %}
```

<br>
### [Makefile](Makefile)

```
{% raw %}
# (c) 2021-2021 Rahmat M. Samik-Ibrahim
# REV02 Fri 23 Jul 2021 22:00:00 WIB
# START Fri 26 Mar 2021 12:07:29 WIB

FILE1=JennyWren

DEPFILES= \
    $(FILE1).tex         \
    01-01.tex            \
    02-01.tex            \
    03-01.tex            \
    04-01.tex            \
    Full-License.tex     \
    mcdumbdumb.jpg       \
    Makefile             \

ALL:	$(FILE1).pdf

$(FILE1).pdf: $(DEPFILES)
	pdflatex $(FILE1)
	pdflatex $(FILE1)
	pdflatex $(FILE1)
	pdflatex $(FILE1)
        # # This is GitHub Page related. You might delete it ###############
	python ../assets/scripts/includeScript.py < LaTeX04.pmd > LaTeX04.md
	cp $(FILE1).pdf /tmp/231.pdf

cleanpdf: clean
	rm -f *.pdf

clean:
	rm -f *.aux *.bbl *.blg *.idx *.log *.out *.toc

xfer:
	chmod 644 $(FILE1).pdf
	cp $(FILE1).pdf ~/tmp/

{% endraw %}
```
