# Makefile for building embedded application.
# by Brian Fraser
# Edited by Divyam and Dante

# Edit this file to compile extra C files into their own programs.
TARGET= as4-morsecode
SOURCES= main.c morsecode.c matrix.c utils.c input.c
PUBDIR = $(HOME)/cmpt433/public/myApps
OUTDIR = $(PUBDIR)
CROSS_TOOL = arm-linux-gnueabihf
CC_CPP = $(CROSS_TOOL)-g++
CC_C = $(CROSS_TOOL)-gcc

CFLAGS = -g -std=c99 -D _POSIX_C_SOURCE=200809L -Werror -Wshadow -Wall -pthread

# -pg for supporting gprof profiling.
#CFLAGS += -pg

all: as4-morsecode

as4-morsecode:
	$(CC_C) $(CFLAGS) $(SOURCES) -o $(OUTDIR)/$(TARGET) $(LFLAGS) -lpthread 

clean:
	rm -f $(OUTDIR)/$(TARGET)

