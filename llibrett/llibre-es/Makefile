FIGS=connex-internet.pdf ordinador4.pdf aplicacio-so.pdf angoixa.pdf triangle.pdf alin-paraules.pdf ibm1/ibm2.pdf ibm1/ibm3.pdf ibm1/ibm4.pdf ibm1/ibm5.pdf

TEX=llibrett-es.tex internet.tex ordinadors-programes.tex ambiguitat.tex bases-dades.tex memories-traduccio.tex tecniques-traduccio-automatica.tex textos-formats.tex intro.tex usos-traduccio-automatica.tex avaluacio-traduccio-automatica.tex problematica-ta-es-ca.tex 
   
all: llibrett-es.pdf

llibrett-es.pdf : $(TEX) $(FIGS) llibrett.bib covington.sty apalikespa.bst
	rubber --pdf llibrett-es

%.pdf: %.eps
	epstopdf $<

%.eps: %.dia
	dia --export=$@ --filter=eps $<

%.eps: %.obj
	tgif -print -eps $<

esborrar:
	rubber --clean llibrett-es
	rm -f *.dvi *.log *.aux *.*~ $(FIGS) *.eps

clean: esborrar
