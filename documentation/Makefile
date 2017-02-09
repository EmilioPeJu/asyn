HTMLFLAGS = --book --duplex --no-numbered --format pdf14 --title --size letter

%.pdf: %.html
	-htmldoc $(HTMLFLAGS) --outfile $@ $<

all: asynDriver.pdf asynRecord.pdf devGpib.pdf doxygen install

doxygen:
	doxygen

install: doxygen
	mkdir -p ../html
	cp -f *.html ../html
	cp -f *.jpg ../html
	cp -f *.png ../html
	cp -f *.pdf ../html
	cp -f -r asynDoxygenHTML ../html
	mkdir -p ../html/gpibCoreConversion ; cp gpibCoreConversion/*html gpibCoreConversion/*css ../html/gpibCoreConversion
	mkdir -p ../html/HowToDoSerial ; cp HowToDoSerial/*.html ../html/HowToDoSerial

clean:
	rm -rf asynDoxygenHTML

realclean: clean
	rm -f *.pdf
