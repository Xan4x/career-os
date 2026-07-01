CV=cv

.PHONY: all clean rebuild

all: $(CV).pdf

$(CV).pdf: $(CV).tex sections/*.tex theme/*.tex
	pdflatex -interaction=nonstopmode -halt-on-error $(CV).tex
	pdflatex -interaction=nonstopmode -halt-on-error $(CV).tex

rebuild: clean all

clean:
	rm -f $(CV).aux $(CV).fdb_latexmk $(CV).fls $(CV).log $(CV).out $(CV).pdf $(CV).synctex.gz
