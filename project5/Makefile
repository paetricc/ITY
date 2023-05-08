#####################################
# Autor: Tomas Bartu                #
# Email: xbartu11@stud.fit.vutbr.cz #
# Datum: 8.5.2023                   #
##################################### 

SHELL=/bin/bash
NAME=proj5
LOGIN=xbartu11
SIZE=-sPAPERSIZE=a4

all: pdflatex

latex: $(NAME).ps
	ps2pdf $(SIZE) $^

$(NAME).ps: $(NAME).dvi
	dvips $(SIZE) $^

$(NAME).dvi: $(NAME).tex
	latex $^
	latex $^

pdflatex: $(NAME).tex
	pdflatex $^
	pdflatex $^

overlay: latex
	pdftk vzor.pdf multibackground $(NAME).pdf output overlay.pdf

zip:
	zip -r $(LOGIN).zip Makefile $(NAME).tex czplain.bst bibliography.bib

# https://www.gnu.org/software/make/manual/html_node/Choosing-the-Shell.html#Choosing-the-Shell
clean:
	rm -rf $(NAME).{aux,dvi,log,ps,fls,synctex.gz,fdb_latexmk,out,bbl,blg,nav,snm,toc} 
