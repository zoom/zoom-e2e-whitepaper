TEX = pdflatex -shell-escape -interaction=nonstopmode -file-line-error

all:
	$(TEX) main.tex
	$(TEX) main.tex
	bibtex main
	$(TEX) main.tex
	$(TEX) main.tex
clean:
	rm -f *aux *blg *log *bbl *dvi *pdf *synctex.gz *.toc *out
