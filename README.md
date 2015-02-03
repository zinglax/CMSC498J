CMSC 498J
==========================================
01-26-2015
hadi amiri

hadi@umd.edu
avw3161

umiacs.umd.edu/~hadi

http://www.umiacs.umd.edu/~hadi/cmsc498j/index.html

# LECTURE01
## Understanding the course
- Social Phenomena
 - Networks
  - Pattern of interconnections
 - Ways contents are preceived in them
  - Deal with various user generated contents

![network](https://encrypted-tbn3.gstatic.com/images?q=tbn:ANd9GcT-RHUm0wvWSUTsnxF3szAD19s6i_8uVkKTrkPnY6Lwh70Vofk1)

### why study networks
- spread of news or disease
- powerful ways at looking at data
- evolution of sciene
- structure of web
- markets modals trades trends
- help understand principles and if they hold or not
- MONEY!!! tracking and communicating with customers 

__WEAK TIES__: links between two nodes that are weak

### computer scientists
- algorithms and models
- 

### Twitter stats
- simple structure
 - followee and follower
- very dynamic structure
 - always changing, creating and deleting is almost the same
- Contents are noisy
 - user generated ubran words
 - often short, context-less, very noisy
 - of streaming type

## What do we learn
- strong and weak ties
 - friends vs aquantiences (strong vs weak ties) 
 - weak ties are better at helping find a job

## Social network clustering
- nodes of one community should be similar
- members of opposite communities they should be dissimilar

## Structural balance
- annotate a networks links
- friend vs enemy 
- how to reason about such networks, tension between two forces

## Structure of the web
- contains a giant strongly connected component
![](http://www9.org/w9cdrom/160/temp.gif)

## Power Laws
- Popularity on a network
![](http://peteashton.com/images/media_power_law_distribution-20090610-000439.jpg)
- The rich get richer

## Link analysis and web search
- Information need us usually small
- links are massive though to feed you that data
- nodes are not equally important

## information cascading
- the behavior that is propagated between nodes
- good looking guy asks you to dance, after asking two others who turned him down, youll probably say no knowing what they said

## homophily and link Prediciton
- Homophily: we tend to share similar characteristics with friends
 - how do we test this
- how can we predict the likelihoot of the existence of a link between two nodes

## Stream processing
- data streams in a rapid rate from different sources
- system cannot store all data
- if data is not processed immediately, it is lost forever
- how do we resond queries about:
 - data, or summaries of data
- Trend Detection and Tracking
 - what are the topics
 - how do topics evolve through time.



# LECTURE02
02-02-2015

## Chapter 2 NCM 

##  Graph Theory
### Arpanet
![](http://personalpages.manchester.ac.uk/staff/m.dodge/cybergeography/atlas/arpanet3.gif)


## Number of nodes in a graph
(N-1)+(N-2)+(N-3)+...+1=n*(n-1)/2 

### Graph density
E = total edges
N = number of nodes

Graph Density = E / (N*(N-1)/2)


think of 6 degrees of contact/connections

### Complete graph
- Graph that has all the possible edges. 
- distance and diameter in a complete graph its always one. 

#### Walk
- A sequence of nodes and edges that starts and ends with nodes where each node is incident to the edges following and preceding it. 

##### Closed Walk Or Cycle 
- A walk with distnct nodes and edges a cycle (ending up at the same place)
#### Trail 
- A trail is a walk in which all edges are distinc although some nodes may be included than once.
#### Path 
- A path is a walk in which all nodes and all edges are distinct.

## Connected Graph
- A graph is connected if every pair of its nodes are reachable from each other


### Shortest path. 
- least number of edges traveled to get from a to b
distance = the length of the shortest path between two nodes

## Sub Graphs
- Take a graph, remove edges/nodes, must be a subset of G

## Types of graphs
- Isomorphics graphs: 1 to 1 mapping between their node that preserves adjacency
- Bipartite graphs: a graph whose vertices can be divided into two disjoint sets and (that is, and are each independent sets) such that every edge connects a vertex in to one in 
- Diagraphs: directed graph (or digraph) is a graph, or set of nodes connected by edges, where the edges have a direction associated with them. ADJ MATRIX M != transpose(M)
- Multigraphs:A multigraph is a graph in which we allow more than one edge to join a pair of vertices. Two or more edges that join a pair of vertices are called parallel edges. Every graph, then, is a multigraph, but not all multigraphs are graphs.
- Hypergraphs: a hypergraph is a generalization of a graph in which an edge can connect any number of vertices. Formally, a hypergraph is a pair where is a set of elements called nodes or vertices, and is a set of non-empty subsets of called hyperedges or edges.




