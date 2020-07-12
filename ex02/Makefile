## MAKEFILE COURSE ##

# Chapter 02: Make all and make [target]

# make [TARGET] -> Executes instructions related to a
#                  specific target.

# The target all has priority over other targets.
# When using "make" command, the first instructions
# executed will be the ones related to the "make all" command,
# because it is the first target listed.

all:
	@echo "make all: First Instruction to be executed"

# type "make less_important" to execute instructions
other_target:
	@echo "this one has less priority than 'make all' "

# it is also possible group many targets in only one
# set of instructions.
# use \ to use more than one line for a single insctruction.
target1 target2 target3:
	@echo "Same command is executed for 'make target1',\
	'make target2'or 'make target3'. "

# running shell commands inside make insctructions:

create_folder:
	@mkdir folder
	# show created directory after its creations
	@ls

delete_folder:
	@rm -rf folder