TEXFILES = $(wildcard *.tex)
PDFFILES = $(TEXFILES:.tex=.pdf)
DVIFILES = $(TEXFILES:.tex=.dvi)
PSFILES  = $(TEXFILES:.tex=.ps)

all: pdf

ps:  $(PSFILES)
pdf: $(PDFFILES)


%.pdf: %.tex
	@rubber --pdf $<
%.ps: %.tex
	@rubber --ps $<
%.dvi: %.tex
	@rubber $<
clean:
	@rubber --clean --pdf $(TEXFILES:.tex=)
	@rubber --clean --ps $(TEXFILES:.tex=)
	@rubber --clean $(TEXFILES:.tex=)

.PHONY: pdf clean all

