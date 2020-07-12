## MAKEFILE COURSE ##

# Chapter 03: Compiling with dependencies and make clean

# Remember: Basic Structure
# [TARGET]: [DEPENDENCIES]
#	[TAB][COMMANDS]

# TARGET: what will be produced with the make [target] command
# DEPENDENCIES: what is needed to produce the [target]
# COMMAND: instructions for building target up from dependencies.


# In this example, we want to produce the file_exec executable file,
# made out from the C++ file file.cpp. There are two ways of doing this:

# 1) Using a single command (make all), that produces directly the
#		 executable (file_exec) from its source file (file.cpp).
#		 since we use only one instruction, we use make all for doing this.

# 2) We can first produce file.o from file.cpp with one command and then
#    produce file_exec from file.o with another one. At first this
#    can sound strange, but it will make sense if we think that file_exec
#    could be a file that is produced from more than one object file,
#		 what is usual when dealing with larger projects.

# when listing a dependency on a Makefile, it will search for another
# instruction containing the dependency name as a target, as can be


# file.cpp is needed to build file.o
all: file.o file.cpp
	g++ file.cpp -o file_exec

# here we will break the command above in two parts:
# 1) g++ -c file.cpp g++   2) g++ file.o -o file_exec

# in order to execute the target "compile", we need file.o
# make will search for the command with file.o as a target.
compile: file.o file.cpp
	@echo "producing executable file..."
	g++ file.o -o file_exec

# when we run "make compile", it will first execute this command
# since it is a dependency.
file.o: file.cpp
	@echo "Compilling file.cpp and producing file.o..."
	g++ -c file.cpp

# after compilation, use "make run" to execute
run:
	@echo "Running file...\n"
	@./file_exec

# if we want to repeat the process, "make clean" will remove the
# produced files.
# note that the target must not have the "clean" name. But normally
# is what is found in most Makefiles.
clean:
	@echo "Removing files..."
	rm file.o file_exec

