TARGET = debug

BASE = scons -j4 target=$(TARGET)
LINUX = $(BASE) platform=linux
WINDOWS = $(BASE) platform=windows
OSX = $(BASE) platform=osx

.PHONY: clean

all:
	make linux
	make windows

clean:
	rm -f *.os

linux:
	make linux32
	make linux64

linux32: SConstruct
	$(LINUX) bits=32

linux64: SConstruct
	$(LINUX) bits=64


windows:
	make windows32
	make windows64

windows32: SConstruct
	$(WINDOWS) bits=32

windows64: SConstruct
	$(WINDOWS) bits=64


osx:
	make osx32
	make osx64

osx32: SConstruct
	$(OSX) bits=32

osx64: SConstruct
	$(OSX) bits=64
