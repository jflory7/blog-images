# This Makefile simplifies building raster images and other
# miscellanea.

help:
	@echo "Type 'make <filename>.jpg' to make JPEG image from SVG"
	@echo "Type 'make <filename>.png' to make PNG image from SVG"

all: help

%.png: %.svg
	@inkscape --without-gui --export-area-page --export-width=1890 --export-file=$@ $<

%.jpg: %.png
	@convert $< $@

.PHONY: clean all help

clean:
	rm -f *.jpg *.png
