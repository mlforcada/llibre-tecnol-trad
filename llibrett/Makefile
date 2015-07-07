all: llibrett.pdf # llibrett.ps

llibrett.pdf : llibrett.tex llibrett.bib angoixa.pdf triangle.pdf ordinador4.pdf covington.sty\
              apalikecat.bst 
	rm -f llibrett.log llibrett.aux llibrett.toc llibrett.blg llibrett.bbl
	pdflatex llibrett
	bibtex llibrett
	pdflatex llibrett
	pdflatex llibrett
	pdflatex llibrett


# llibrett.ps : llibrett.tex llibrett.bib angoixa.eps triangle.eps covington.sty\
#               apalikecat.bst
# 	rm -f llibrett.log llibrett.aux llibrett.toc llibrett.blg llibrett.bbl
# 	latex llibrett
#	bibtex llibrett
#	latex llibrett
#	latex llibrett
#	latex llibrett
#  	dvips -o llibrett.ps llibrett


angoixa.pdf : angoixa.eps
	epstopdf angoixa.eps

triangle.pdf : triangle.eps
	epstopdf triangle.eps

ordinador4.pdf : ordinador4.eps
	epstopdf ordinador4.eps

angoixa.eps : angoixa.obj
	tgif -print -eps angoixa.obj

triangle.eps : triangle.obj
	tgif -print -eps triangle.obj

ordinador4.eps : ordinador4.obj
	tgif -print -eps ordinador4.obj

esborrar:
	rm -f *.dvi *.log *.aux *.*~ ordinador4.pdf triangle.pdf angoixa.pdf *.eps
