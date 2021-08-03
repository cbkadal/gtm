# (c) 2021-2021 Rahmat M. Samik-Ibrahim
# REV00 Tue 03 Aug 2021 13:41:25 WIB
# START Tue 03 Aug 2021 13:41:25 WIB

FILE1=Grounded-Theory-Copy-And-Paste

DEPFILES= \
    $(FILE1).tex         \
    01-01.tex            \
    02-01.tex            \
    03-01.tex            \
    04-01.tex            \
    Full-License.tex     \
    ucls-coat.jpg        \
    Makefile             \

ALL:	$(FILE1).pdf

$(FILE1).pdf: $(DEPFILES)
	pdflatex $(FILE1)
	pdflatex $(FILE1)
	pdflatex $(FILE1)
	pdflatex $(FILE1)

cleanpdf: clean
	rm -f *.pdf

clean:
	rm -f *.aux *.bbl *.blg *.idx *.log *.out *.toc

