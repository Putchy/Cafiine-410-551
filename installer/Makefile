CC=powerpc-eabi-gcc
CFLAGS=-nostdinc -fno-builtin -c
LD=powerpc-eabi-ld
LDFLAGS=-Ttext 1800000 --oformat binary
project	:=	src
root:=.
build	:=	 $(root)/bin
libs := $(root)../../libwiiu/bin
www :=$(root)../../www
framework:=$(root)../../framework
all: setup main550 main532 main500 main410 main400
setup:
	mkdir -p $(root)/bin/
main550:
	$(CC) $(CFLAGS) -DVER=550 $(project)/*.c
	#-Wa,-a,-ad
	cp -r $(root)/*.o $(build)
	rm $(root)/*.o
	$(LD) $(LDFLAGS) -o $(build)/code550.bin $(build)/loader.o `find $(build) -name "*.o" ! -name "loader.o"`
main532:
	$(CC) $(CFLAGS) -DVER=532 $(project)/*.c
	#-Wa,-a,-ad
	cp -r $(root)/*.o $(build)
	rm $(root)/*.o
	$(LD) $(LDFLAGS) -o $(build)/code532.bin $(build)/loader.o `find $(build) -name "*.o" ! -name "loader.o"`
main500:
	$(CC) $(CFLAGS) -DVER=500 $(project)/*.c
	#-Wa,-a,-ad
	cp -r $(root)/*.o $(build)
	rm $(root)/*.o
	$(LD) $(LDFLAGS) -o $(build)/code500.bin $(build)/loader.o `find $(build) -name "*.o" ! -name "loader.o"`
main410:
	$(CC) $(CFLAGS) -DVER=410 $(project)/*.c
	#-Wa,-a,-ad
	cp -r $(root)/*.o $(build)
	rm $(root)/*.o
	$(LD) $(LDFLAGS) -o $(build)/code410.bin $(build)/loader.o `find $(build) -name "*.o" ! -name "loader.o"`
main400:
	$(CC) $(CFLAGS) -DVER=400 $(project)/*.c
	#-Wa,-a,-ad
	cp -r $(root)/*.o $(build)
	rm $(root)/*.o
	$(LD) $(LDFLAGS) -o $(build)/code400.bin $(build)/loader.o `find $(build) -name "*.o" ! -name "loader.o"`
clean:
	rm -r $(build)/*
