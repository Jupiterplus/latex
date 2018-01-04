LATEX=xelatex
LATEX_COMPILE_OPTS=-pdf -bibtex -dvi-
LATEX_CLEAN_OPTS=-c
LATEX_VERYCLEAN_OPTS=-C
LATEX_MAIN_FILE=main.tex
PDF_FILE_TOVIEW=bitcoin.pdf

all: $(PDF_FILE_TOVIEW)

$(PDF_FILE_TOVIEW) : main.pdf
	@\cp $< $@

CMake-tutorial.pdf : $(LATEX_MAIN_FILE)
	@$(LATEX) $(LATEX_COMPILE_OPTS) $<

rebuild: clean
	@$(LATEX) $(LATEX_VERYCLEAN_OPTS) $(LATEX_COMPILE_OPTS) $(LATEX_MAIN_FILE) 2> /dev/null
	@echo "You may now rebuild with 'make'"
clean:
	# @$(LATEX) $(LATEX_CLEAN_OPTS) $(LATEX_COMPILE_OPTS) $(LATEX_MAIN_FILE) 2> /dev/null
	@-\rm -f *.vrb *.snm *.nav *.log *.aux *.out *.toc
