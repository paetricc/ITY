#####################################
# Autor: Tomas Bartu                #
# Email: xbartu11@stud.fit.vutbr.cz #
# Datum: 20.3.2023                  #
##################################### 

SHELL=/bin/bash
NAME=proj3
LOGIN=xbartu11
SIZE=-sPAPERSIZE=a4

all: latex overlay

latex: $(NAME).ps
	ps2pdf $(SIZE) $^

$(NAME).ps: $(NAME).dvi
	dvips $(SIZE) $^

$(NAME).dvi: $(NAME).tex
	latex $^
	latex $^

pdflatex: $(NAME).tex
	pdflatex $^

overlay: latex
	pdftk vzor.pdf multibackground $(NAME).pdf output overlay.pdf

# https://www.gnu.org/software/make/manual/html_node/Choosing-the-Shell.html#Choosing-the-Shell
clean:
	rm -rf $(NAME).{aux,dvi,log,ps,fls,synctex.gz,fdb_latexmk,out} 
