.PHONY: all clean texfirst builddir

builddir:
	mkdir -p build

texfirst: ${IMAGES} | builddir
	xelatex -output-directory=build slides.tex

clean:
	rm -r build/

all: texfirst
