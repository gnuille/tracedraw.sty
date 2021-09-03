
.PHONY: all clean distclean
PDFS=$(patsubst %.tex,%.pdf,$(wildcard *.tex))

all: $(PDFS)
	$(MAKE) clean

%.pdf: %.tex
	latexmk -pdf $<

clean:
	latexmk -c

distclean:
	latexmk -C
	
