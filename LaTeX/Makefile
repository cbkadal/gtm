# (c) 2021-2021 Rahmat M. Samik-Ibrahim
# REV03 Thu 05 Aug 2021 11:35:55 WIB
# REV02 Fri 23 Jul 2021 22:00:00 WIB
# START Fri 26 Mar 2021 12:07:29 WIB

FILE1=Copy-And-Paste

DEPFILES= \
    $(FILE1).tex  \
    01-01.tex     \
    02-01.tex     \
    03-01.tex     \
    04-01.tex     \
    bib.bib       \
    End.tex       \
    ucls-coat.jpg \
    Makefile      \


ALL:	$(FILE1).pdf

$(FILE1).pdf: $(DEPFILES)
	pdflatex $(FILE1)
	pdflatex $(FILE1)
	bash .shsh
	pdflatex $(FILE1)
	pdflatex $(FILE1)
	rm -f *.aux *.bbl *.bcf *.blg *.idx *.log *.out *.toc

cleanpdf: clean
	rm -f *.pdf

clean:
	rm -f *.aux *.bbl *.blg *.idx *.log *.out *.toc


