# EECE5155-Project-Code

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
	
## Roadmap
1.	Project goals and objectives
	1.	Simulate multi-layer topology (fog-edge layered network) on NS-3 
		1.	Simulate simple edge network
		2.	Add fog layer 
		3.	Add the rest of the devices to the edge network (fully simulating the multi-layer topology)
	2.	Configure sending and receiving nodes
	3.	Configure data specific type nodes (GPS, streaming, downloading, and combo)
	4.	Implement 6LoWPAN data communication protocol on simulated network 
	5.	Implement AJIA data reliability protocol on simulated network
	6.	Configure FIFO load balancing algorithm on edge and fog nodes 
	7.	Configure EDF load balancing algorithm on edge and fog nodes
	8.	Configure LAT load balancing algorithm on edge and fog nodes
	9.	Set up performance and reliability measuring matrixes on all nodes (latency and packet error rate)
	10.	Perform experiment to collect data on the following configurations: FIFO with 6LoWPAN, FIFO with AJIA, EDF with 6LoWPAN, EDF with AJIA, LAT with 6LoWPAN, and LAT with AJIA.
	11.	Analysis of data
	12.	Complete paper
	13.	Complete presentation
2.	Timeline 
	1.	19 October 1115 – 1200: Roadmap planning
	2.	26 October 11:15am – 1:15pm: topology simulation 
	3.	28 October 2:00pm – 4:00pm: topology cont.
	4.	2 November 11:15am – 1:15pm: implement data protocols and algorithms
	5.	9 November 11:15am – 1:15pm: perform experiments and collect data
	6.	16 November 11:15am – 1:15pm: divide and conquer paper (due 20 Nov)
	7.	30 November 11:15am – 1:15pm: presentation (due 6 Dec)
	8.	(complete meeting topic NLT the next meeting. For example, topology simulation must be completed by 2 November)
3.	Important milestones/deliverables
	1.	Paper due 20 November
	2.	Presentation due 6 December
4.	Possible risks
	1.	NS-3 unable to simulate multi-layered edge fog network -> try mininet 
5.	Dependencies
	1.	Simulation of topology required before anything else
6.	Takeaways
	1.	Individually find tutorials on simulations for the topologies on NS-3 
	
## TO-DO
- [ ] Everyone get https://github.com/subinjp/edgecomputing/ example topology working on their own machines (NLT 28 October meeting)
