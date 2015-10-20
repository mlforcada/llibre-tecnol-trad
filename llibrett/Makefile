FIGS=angoixa.pdf triangle.pdf ordinador4.pdf aplicacio-so.pdf

all: llibrett.pdf

llibrett.pdf : llibrett.tex llibrett.bib $(FIGS) covington.sty apalikecat.bst 
	rubber --pdf llibrett

%.pdf: %.eps
	epstopdf $<
	
%.eps: %.dia
	dia --export=$@ --filter=eps $<
		
%.eps: %.obj
	tgif -print -eps $<
			
esborrar :
	rubber --clean llibrett
	rm -f *.dvi *.log *.aux *.*~ $(FIGS) *.eps

clean : esborrar
