FIGS=angoixa.pdf triangle.pdf ordinador4.pdf aplicacio-so.pdf \
     connex-internet.pdf

TEX=ambiguitat.tex avaluacio-traduccio-automatica.tex bases-dades.tex \
    experiencies-ta-es-ca.tex internet.tex intro.tex llibrett.tex \
    memories-traduccio.tex ordinadors-programes.tex \
    problematica-ta-es-ca.tex tecniques-traduccio-automatica.tex \
    textos-formats.tex usos-traduccio-automatica.tex

all: llibrett.pdf

llibrett.pdf : $(TEX) $(FIGS) llibrett.bib covington.sty apalikecat.bst 
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
