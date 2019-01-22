TEX      = xelatex
TEXFLAGS = -interaction=nonstopmode

clean:
	-rm *.aux
	-rm *.bbl
	-rm *.blg
	-rm *.log
	-rm *.out

%:
	cd $<
	echo $<
	pwd
	$(TEX) $(TEXFLAGS) $<.tex
	$(TEX) $(TEXFLAGS) $<.tex
