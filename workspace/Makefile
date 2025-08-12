# Makefile for building LaTeX with biber and cleaning up

MAIN = main

all: pdf clean

pdf:
	pdflatex $(MAIN).tex
	biber $(MAIN)
	pdflatex $(MAIN).tex
	pdflatex $(MAIN).tex

clean:
	rm -f $(MAIN).aux $(MAIN).bbl $(MAIN).blg $(MAIN).log \
	      $(MAIN).out $(MAIN).toc $(MAIN).lof $(MAIN).lot \
	      $(MAIN).bcf $(MAIN).run.xml $(MAIN).fdb_latexmk \
	      $(MAIN).fls $(MAIN).dvi
