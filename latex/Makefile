TARGET=adonath-cv
LATEX=pdflatex
BIBTEX=bibtex

all: $(TARGET).pdf

# $(TARGET).pdf: *.tex figures/* text/* tables/* $(TARGET).bib
$(TARGET).pdf: *.tex $(TARGET).bib

%.pdf: %.tex
	$(LATEX) $<
	$(BIBTEX) $*
	$(LATEX) $<
	$(LATEX) $<

make clean:
	- rm -f $(TARGET).pdf $(TARGET).aux $(TARGET).log $(TARGET).bbl $(TARGET).fff
	- rm -f *.aux */*.aux */*/*.aux *.out *.xml *.mtc* *.blg

