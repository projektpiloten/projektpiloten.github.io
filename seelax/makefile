
all:	extract-pages extract-images
		
extract-pages:	#
				for i in $$(seq 13); do echo $$i; pdf2svg portfolio-seelax-hq.pdf page$$(printf "%02d" $$i)-hq.svg $$i; done
	
extract-images:	#
				for f in page??-hq.svg; do echo "extracting images from $$f"; ./extract_embedded_images_from_svg.py -p img/$$(basename $$f .svg) $$f; done

make-progressive:	#
				# fish -c "cd img; for f in *.jpg; echo $f; convert $f -strip -interlace Plane -resize 2000x\> -quality 80 (echo $f|sed -e 's/-hq//g' -e 's/.jpg/-web.jpg/g'); end"