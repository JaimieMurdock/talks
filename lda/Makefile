# name without .tex
LATEXFILE = slides

pdf : $(LATEXFILE).pdf

$(LATEXFILE).pdf : $(LATEXFILE).tex
	inkscape -D -z --file=img/lda.svg --export-pdf=lda.pdf # --export-latex
	pdflatex -shell-escape $(LATEXFILE)
	bibtex $(LATEXFILE)
	pdflatex -shell-escape $(LATEXFILE)
	pdflatex -shell-escape $(LATEXFILE)

clean :
	rm -f *.dvi *.bbl *.aux *.log *.blg *.toc *.nav *.out *.pyg *.snm
	rm -f $(LATEXFILE).pdf
	rm -f lda.pdf
	rm -f lda.pdf_tex
