#####################################
# Autor: Tomas Bartu                #
# Email: xbartu11@stud.fit.vutbr.cz #
# Datum: 20.2.2023                  #
##################################### 

SHELL=/bin/bash
NAME=proj1
LOGIN=xbartu11

latex: $(NAME).ps
	ps2pdf $^

$(NAME).ps: $(NAME).dvi
	dvips -t a4 $^

$(NAME).dvi: $(NAME).tex
	latex $^
	latex $^

pdflatex: $(NAME).tex
	pdflatex $^

# https://www.gnu.org/software/make/manual/html_node/Choosing-the-Shell.html#Choosing-the-Shell
clean:
	rm -rf $(NAME).{aux,dvi,log,ps,fls,synctex.gz,fdb_latexmk,out} 