## MAKEFILE COURSE ##

# Chapter 05: Phony Targets

# A phony target is the target that has not the name of a specific
# file. It is only a name for a recipe to be executed when an
# explicit request is made. Phony targets are used to avoid
# possible conflicts with a file with the same name as the target,
# and also for improving performance.

# in this example, we will add an empty clean to our
# project, and also the clean instruction, that only
# will prints something.


all: create_file clean

create_file:
	@echo "1) Creating clean file...\n"
	@touch clean

# if we comment the line above, the commands from the phony_file target
# will not be executed, because there is already a file named "phony_file"
# on the project directory.
.PHONY: clean
clean:
	@echo "2) This is only the clean insctruction!"
	@echo "It is not the recipe for the clean file!\n"
	@echo "Please comment the '.PHONY: clean' line if "
	@echo "related to the file with the same name."

# When .PHONY is added to the clean target, the second set of prints
# commands is executed. Otherwise, a confusion will be made between the
# clean instruction and the clean file.