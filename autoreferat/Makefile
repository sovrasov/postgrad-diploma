.PHONY: all clean texfirst texsecond builddir refs

builddir:
	mkdir -p build

texfirst: ${IMAGES} | builddir
	xelatex -output-directory=build paper.tex

refs: texfirst
	cp ../bibliography.bib ./build
	cd ./build ;	pwd ;	biber paper

texsecond: refs
	xelatex -output-directory=build paper.tex

clean:
	rm -r build/

all: texsecond
