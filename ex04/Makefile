## MAKEFILE COURSE ##

# Chapter 04: more than one dependency

# In this chapter, we will use a Makefile to compile a
# project on C language. It is composed by two source files
# (file.c and print_main.c) and a header file (file.h)

# Folder Strucutre

# build   : contains output files (.o)
# bin     : contains executable files
# src     : contains source files (.c)
# include : contains header files (.h)


# make all will produce the file_exec
# using both object files (print_main.o and file.o)

all: print_main.o file.o
	gcc build/print_main.o build/file.o -o bin/file_exec

# same as make all, but with dependencies not explicit.
# withou obtaining the object files first,
# running this will return an error.
file_exec:
	gcc build/print_main.o build/file.o -o bin/file_exec

# use this to produce both object files and run make file_exec later
compile:
	gcc -c src/file.c -I include/ -o build/file.o
	gcc -c src/print_main.c -o build/print_main.o

# obtain only file.o object file
file.o:
	gcc -c src/file.c -I include/ -o build/file.o

# obtain only print_main.o object file
print_main.o:
	gcc -c src/print_main.c -o build/print_main.o

# execute program
run:
	@echo "\nRunning program...\n\n"
	@./bin/file_exec

# cleaning for newer build process.
clean:
	rm build/*.o bin/*