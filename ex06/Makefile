## MAKEFILE COURSE ##

# Chapter 06: Implicit Commands

# make has some coupling with GCC. Therefore, there are some
# simplifications that can be made with implicit commands.

# in this example, we will produce a executable named 'file',
# made out of the made.o file, that is produced after the compilation
# of file.c

# If we	dont write the commands for the following,
# targets it will be implicitly understood that:

# 1) [FILENAME] has the dependency of [FILENAME].o and
#    can be produced as cc [FILENAME].o -o [FILENAME]

# 2) [FILENAME].o has the dependency of [FILENAME].c and
#    can be produced as cc -c o [FILENAME].o [FILENAME].C

#
file:

file.o:

# file.c is a source file so you can either write it or not.
# file.c:

# execute program
run:
	@echo "\nRunning program...\n\n"
	@./file

# cleaning for newer build process.
clean:
	rm file file.o