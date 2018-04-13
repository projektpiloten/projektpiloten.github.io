
all:	extract-pages extract-images
		
extract-pages:	#
				for i in $$(seq 13); do echo $$i; pdf2svg portfolio-seelax-hq.pdf page$$(printf "%02d" $$i)-hq.svg $$i; done
	
extract-images:	#
				for f in page??-hq.svg; do echo "extracting images from $$f"; ./extract_embedded_images_from_svg.py -p img/$$(basename $$f .svg) $$f; done