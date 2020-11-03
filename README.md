# EECE5155-Project-Code

## Instructions for running topology
1. NS-3 installation https://www.nsnam.org/docs/tutorial/html/index.html
2. `cd source/ns-3/`
3. 	```bash
	./waf
	./waf --run scratch/<filename>
	```
## Questions for the instructor
1. How can we send custom data to nodes on ns-3?
	develop an application - application layer will talk to the transport layer.
	What do we have at each layer of our protocols: 6LoWPAN (network layer), 806.4 (physical layer); we want to send our own packets from one node to another node.
	Nodes will send what is at the application layer. We are using the 6LoWPAN and modifying this to send our own data.
2. How to use PCAP on 6LoWPAN in ns3?
	Not all code can incorporate packet tracing. Instead, have stuff logged to file or screen (such as timestamping all packets for when you send and receive it)
3. Does he recommend utilizing another simulating software?
	No - utilize NS-3 cause this is utilized for research and industry development.
	
## Simulation 
1. Applications on all nodes (telling node to either compute or send data to another node to compute; specifying processing strength of node; specify data rate (latency) on links)
2. Two layers of the network (edge layer and fog layer)
3. Edge layer contains 9 containers of weapon systems; each "weapon system" contains 3 edge devices
4. All edge devices connect to one gateway on the fog network (3 weapon systems per gateway)
5. Three gateway devices are on fog network and all are connected to one another
6. All edge devices within weapon systems, and the link between edge devices and their fog gateway are 6LoWPAN and CSMA
7. All gateways in the fog layer are point-to-point devices 

## Single Weapon System Container/Edge Network Topology
```
      n0                                      n1            n2
  +---------+                             +--------+     +--------+
  | UDP     |          fog node           | UDP    |     | UDP    |
  +---------+    +---------+--------+     +--------+     +--------+
  | IPv6    |    | IPv6    | IPv6   |     | IPv6   |     | IPv6   |
  +---------+    +---------+--------+     +--------+     +--------+
  | 6LoWPAN |    | 6LoWPAN | 6LoWPAN|     | 6LoWPAN|     | 6LoWPAN|
  +---------+    +---------+--------+     +--------+     +--------+
  | CSMA    |    | CSMA    | CSMA   |     | CSMA   |     | CSMA   |  
  +---------+    +---------+--------+     +--------+     +--------+
       |              |    |   |               |               |
       ================    |   =================               | 
                           =====================================
```

## Fog Layer Topology
```
n0 -------------- n1
 \                /
  \              /
   \            /
         n2
point-to-point links
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
