CXX = mpic++
CXXFLAGS = -g3 -Wall
MKDIR = mkdir -p

LIBS=-lm -lmpi

directorios: 
	$(MKDIR) build dist

main.o: directorios main.cpp
	$(CXX) $(CXXFLAGS) -c main.cpp -o build/main.o

#utilidades.o: directorios utilidades.c utilidades.h
#	$(CXX) $(CXXFLAGS) -c utilidades.c -o build/utilidades.o

all: clean main.o
	$(CXX) $(CXXFLAGS) $(LIBS) -o dist/programa build/main.o
	rm -fr build

clean:
	rm -fr *.o a.out programa dist build

.DEFAULT_GOAL := all