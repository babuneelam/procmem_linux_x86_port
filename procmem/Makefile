
BUILDDIR=../bin
SHELL = /bin/sh
CC    = gcc
FLAGS        = -std=gnu99 -Iinclude
CFLAGS       = -fPIC -pedantic -march=native -ggdb3
DEBUGFLAGS   = -O0 -D _DEBUG
RELEASEFLAGS = -O2 -D NDEBUG -combine -fwhole-program
LIBPATH=../bin/

TARGET  = procmem
SOURCES = $(shell echo *.c)
OBJECTS = $(SOURCES:.c=.o)

all: dir $(BUILDDIR)/$(TARGET)

dir:
	mkdir -p $(BUILDDIR)

$(BUILDDIR)/$(TARGET): $(OBJECTS)
	$(CC) $(FLAGS) $(CFLAGS) $(DEBUGFLAGS)i -L$(LIBPATH) -o $(BUILDDIR)/$(TARGET) $(OBJECTS) -lpagemap

clean:
	$(RM) *.o
	$(RM) $(BUILDDIR)/$(TARGET)
