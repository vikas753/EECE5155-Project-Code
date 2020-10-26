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
I.	Project goals and objectives
	a.	Simulate multi-layer topology (fog-edge layered network) on NS-3 
		i.	Simulate simple edge network
		ii.	Add fog layer 
		iii.	Add the rest of the devices to the edge network (fully simulating the multi-layer topology)
	b.	Configure sending and receiving nodes
	c.	Configure data specific type nodes (GPS, streaming, downloading, and combo)
	d.	Implement 6LoWPAN data communication protocol on simulated network 
	e.	Implement AJIA data reliability protocol on simulated network
	f.	Configure FIFO load balancing algorithm on edge and fog nodes 
	g.	Configure EDF load balancing algorithm on edge and fog nodes
	h.	Configure LAT load balancing algorithm on edge and fog nodes
	i.	Set up performance and reliability measuring matrixes on all nodes (latency and packet error rate)
	j.	Perform experiment to collect data on the following configurations: FIFO with 6LoWPAN, FIFO with AJIA, EDF with 6LoWPAN, EDF with AJIA, LAT with 6LoWPAN, and LAT with AJIA.
	k.	Analysis of data
	l.	Complete paper
	m.	Complete presentation
II.	Timeline 
	a.	19 October 1115 – 1200: Roadmap planning
	b.	26 October 11:15am – 1:15pm: topology simulation 
	c.	28 October 2:00pm – 4:00pm: topology cont.
	d.	2 November 11:15am – 1:15pm: implement data protocols and algorithms
	e.	9 November 11:15am – 1:15pm: perform experiments and collect data
	f.	16 November 11:15am – 1:15pm: divide and conquer paper (due 20 Nov)
	g.	30 November 11:15am – 1:15pm: presentation (due 6 Dec)
	h.	(complete meeting topic NLT the next meeting. For example, topology simulation must be completed by 2 November)
III.	Important milestones/deliverables
	a.	Paper due 20 November
	b.	Presentation due 6 December
IV.	Possible risks
	a.	NS-3 unable to simulate multi-layered edge fog network -> try mininet 
V.	Dependencies
	a.	Simulation of topology required before anything else
VI.	Takeaways
	a.	Individually find tutorials on simulations for the topologies on NS-3 
	
## TO-DO
[] Everyone get https://github.com/subinjp/edgecomputing/ example topology working on their own machines (NLT 28 October meeting)
