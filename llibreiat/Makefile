all: llibreiat.pdf # llibreiat.ps

llibreiat.pdf : llibreiat.tex llibreiat.bib angoixa.pdf triangle.pdf covington.sty\
              apalikecat.bst
	rm -f llibreiat.log llibreiat.aux llibreiat.toc llibreiat.blg llibreiat.bbl
	pdflatex llibreiat
	bibtex llibreiat
	pdflatex llibreiat
	pdflatex llibreiat
	pdflatex llibreiat


# llibreiat.ps : llibreiat.tex llibreiat.bib angoixa.eps triangle.eps covington.sty\
#               apalikecat.bst
# 	rm -f llibreiat.log llibreiat.aux llibreiat.toc llibreiat.blg llibreiat.bbl
# 	latex llibreiat
#	bibtex llibreiat
#	latex llibreiat
#	latex llibreiat
#	latex llibreiat
#  	dvips -o llibreiat.ps llibreiat


angoixa.pdf : angoixa.eps
	epstopdf angoixa.eps

triangle.pdf : triangle.eps
	epstopdf triangle.eps

angoixa.eps : angoixa.obj
	tgif -print -eps angoixa.obj

triangle.eps : triangle.obj
	tgif -print -eps triangle.obj

esborrar:
	rm -f *.dvi *.log *.aux *.*~ triangle.pdf angoixa.pdf *.eps
