NAME=proj5

$(NAME).pdf: $(NAME).ps
		ps2pdf $(NAME).ps

$(NAME).ps: $(NAME).dvi
		dvips $(NAME).dvi

$(NAME).dvi: $(NAME).tex 
		latex $(NAME).tex
		bibtex $(NAME)
		latex $(NAME).tex
		latex $(NAME).tex
clean:
		-rm $(NAME).ps $(NAME).dvi $(NAME).aux  $(NAME).log $(NAME).out $(NAME).toc $(NAME).snm $(NAME).nav $(NAME).blg $(NAME).bbl
zipit:
		zip xplagi0b-fit.zip $(NAME).tex Makefile czechiso.bst $(NAME).bib codeexample.c
