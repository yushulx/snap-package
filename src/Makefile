CC=gcc
CCFLAGS=-c

LDFLAGS=-L ./lib
DBRLIB=-lDynamsoftBarcodeReader

STDLIB=-lstdc++

TARGET=barcode-reader
OBJECT=ReadBarcode.o
SOURCE=ReadBarcode.cpp

# build rule for target.
$(TARGET): $(OBJECT)
	$(CC) -o $(TARGET) $(OBJECT) $(STDLIB) $(DBRLIB) $(LDFLAGS)

# target to build an object file
$(OBJECT): $(SOURCE)
	$(CC) $(CCFLAGS) $(SOURCE)

install:
	mkdir -p $(DESTDIR)/usr/bin/
	cp ./barcode-reader $(DESTDIR)/usr/bin/
	mkdir -p $(DESTDIR)/usr/lib
	cp ./lib/libDynamsoftBarcodeReader.so $(DESTDIR)/usr/lib

# the clean target
.PHONY : clean
clean: 
	rm -f $(OBJECT) $(TARGET)

