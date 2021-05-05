# A simple Makefile for compiling small SDL projects

# set the compiler
CC := g++

# set the compiler flags
CFLAGS := `sdl2-config --libs --cflags` -ggdb3 -O0 --std=c99 -Wall -lSDL2_image -lm
# add header files here
HDRS :=

# add source files here
SRCS := main.cpp

# generate names of object files
OBJS := $(SRCS:.cpp=.o)

# name of executable
EXEC := main

# default recipe
all: $(EXEC)

main: main.cpp Makefile
	$(CC) -o $@ $@.cpp $(CFLAGS) $(LIBS)

# recipe for building the final executable
$(EXEC): $(OBJS) $(HDRS) Makefile
	$(CC) -o $@ $(OBJS) $(CFLAGS)

# recipe for building object files
#$(OBJS): $(@:.o=.c) $(HDRS) Makefile
#    $(CC) -o $@ $(@:.o=.c) -c $(CFLAGS)

# recipe to clean the workspace
clean:
	rm -f $(EXEC) $(OBJS)

.PHONY: all clean
