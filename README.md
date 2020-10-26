# EECE5155-Project-Code

----------------------------------------------------------------
One stop place for code submissions for EECE5155 Project work 
----------------------------------------------------------------

## Instructions for running topology
1. `git clone <repo>`
2. `cd <repo>/src/ns-allione-3.25/bake`
3. 	```bash
	$ export BAKE_HOME=`pwd`
	$ export PATH=$PATH:$BAKE_HOME:$BAKE_HOME/build/bin
	$ export PYTHONPATH=$PYTHONPATH:$BAKE_HOME:$BAKE_HOME/build/lib
	$ ./bake.py configure -e ns-3.25
	$ ./bake.py check
	$ ./bake.py download
	$ ./bake.py build
	```
4. `cd ..`
5. `cd ns-3.25`
6. 	```bash
	./waf configure`
	./waf
	./waf --run scratch/<filename>
	```
