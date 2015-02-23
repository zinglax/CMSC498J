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


# LECTURE03
02-04-2015

BFS and shortest path algorithms
## Smallest world phenomenon
- how are all of us connected 
- mapping between all of the things we track and collect data on.

__connected components__: of a graph is a subset of nodes such that every node in the subset has a path to every other; and the subset is not part of a bigger component. 

## Bredth-first search
- A general technique for  traversing graphs.
- can determin if the graph is connect or not. can find connected components
- can deterimine shortests paths in terms of the number of edges between nodes.
### How to find connectedness
- start with s
- vist all neighbors of s (these are called level-1 nodes)
- vist all neighbors of level-1 nodes (these are called level-2 nodes)
- continue...

- is there any nodes that are not touched. if so then you found a connected component of the overall graph

### Dijkstras
- weighted directed graph
- source node then destination node and then take the shortest

# LECTURE04
02-09-2015

## Strong vs Weak Ties
- Granovetter's Experiment
- weak ties become more important when getting a job


## Triadic Closure
- If two people in a network have a friend in commo, then there is an increased liklihood they will become friends themselves 
- The term 'triadic closure' comes from the fact that the B-C edge has the effect of closing the triangle or triangle closure
- watching a network for a longer period of time:
 -Multiple edgesform!
        - some form through triadic closure while others (such as d-g) form even through the two endpoins. 
- Reasons for triadic closure
 - Opportunity:
   - B and C have a common friend A -> ther is an increased chance they will end up knowing each other
  - Trust:
   - B and C arefriends with A -> gives them a basis for trusting each other that an arbitrary pair of unconnected people might lack
 - Incentive:
  - A may have to bring B and C together (social psychology)                

## Clustering Coefficient
- A measure to capture the prevalence of Triacic closure
- Clustering coefficient
 - Cf of a node A is defined as the probability that two randomly selected frinds of a are friends with eachother
  - CF(A) = number ofconnectioons btw A's friends / possible number of connections btw A's friends
  - Range is from 0 - 1 
  - Basically making a clique with the node your interested in and its neighbors. 
    
- emperical study
  - teenage girls who have a low clustering coefficient in their network of firends are significantly more likely to contemplate suicicde than those whose clustering coefficient is high    
    
## Bridges and local bridges
- Structural Notation!
- The Edge (A,B) is called a bridge if deleting it would put A and B in two different connected component
  - Bridges are rare in social networks
- _Local bridges_: an edge E(A,B) is a local bridge if its endpoints A and B have no friends in common
  - In other words, if deleting the edge wiould increase the distance btw A and B to a value strictly more than 2
  - A local bridge cannot be part of a triangle
- a Local Bridge with a large span. 
  - span of a local bridge is the distance betwee its endpoins if the edge were deleted

- why acquanticences are more important (weak ties)
  - A, C, D, and E will all tend to be exposed to similar sources of info, while A's link to B offers her access to things she otherwise wouldn't necessarily hear about
  
- End points of a bridge have no friends in common

  
## Strong triadic closure
### Links in networks have strength
- friendship nets (closed friends vs acquantiences)
- Telco Nets (amount of talking time on the phone)
### We characterize edges
- strong (correspoinding with friends), or
- weak (corresponding to acquaintances)
   
### Strong triadic closure
- if A has a strong links to B and C, then there must be a link, either weak or strong, btw B and C!


## The strength of weak ties
- the argument is that the weak ties (acquaintances) are social ties that connect us to new sources of information, and teir conceptual "span" in the social network (the local bridge property) is directly related to their weakness as social ties
- this duel role -as weak connections but also valuable linkes to hard-to-reach parts of the network
 - is the suprizing strength of weak ties
 
- We defined bridges:
 - edges with nodes in different connected components.
- We defined local bridges as:
 - edges not in triangles!
- We defined two types of edges:
 - Strong and Weak Ties
- An edge is:
 - either strong or weak, and
 - either local bridge or not local bridge!
- We defined strong triadic closure:
 - Two strong ties imply a third strong / weak tie
- We discussed local bridges are weak ties

### tie strength in real world nets
- neighborhood overlap of an edge connecting nodes A and B:
- Number of nodes who are neighborsof both a and B/ number of nodes who are neighbors of at least one of A or B


# LECTURE05
02-11-2015

## centrality
- what characters an important node in a network?
 - Most influential people in social nets
 - Key infastructure nodes 
 
## Centrality measures
most are similar to eachother
- Different centrality measures capture different structural characteristics of nodes
- There is usually a high correlation between these measures
- Sometimes the most central node might depend on which measure is used

### Degree centrality
- A node is central if it has ties to many other nodes
 - Look at the degree of the node (NUMBER OF NEIGHBORS)
 - Adjacency Matrix is helpful
 
### Standardized Degree Centrality
- take the degree and divide by the maximum possible degree centrality value!

### Closeness Centrality
- a node is central if it is "close" to other nodes
 - look at the disance between the nodes
 - Closeness: 1/ Distance between nodes
- Standardized Closeness Centrality
 - Divide by the maximum possible closeness centrality value!
 - 1/(N-1)
- WAIT, WHAT ABOUT UNCONNECTED GRAPHS
 - How to compute Closeness Centrality in networks with disconnected components?
  - Only consider the giant component or do graph something?
  - Only consider nodes that are reachable in paths of length, 1,2,...,k this is called a k Reach step
 
## Betweenness Centrality
- A node is cental if other nodes have to go through it to get to each other
 - Look at shortest paths between nodes
 - For each pair of nodes, compute the shortest paths between them.
 - For each pair of nodes, determine the fraction of shortest paths that pass through a target node
 - Sum the fractions over all pairs of nodes.
 
- standardized Betweennes Centrality
 - Divide by the mazximum possible betweenness centrality value
  - (N-1(N-2)/2: the number of other pairs of nodes (exclude the node itself)
 
## Clustering
- aim to develp techniques to idenitify densely connected regions
 - Breaking a network into a set of densely connected nodes
 - with sparse connections between groups
 
### Divisive methods
- breaking the graph into different sections starting from the whole graph
- Important: Bridges connect tightly-knit groups in networks
 - to find clusters, remove bridges and local bridges. 
 - Bridges are rare though in realworld graphs
 - Issue1: when there are several bridges, which one should we choose
 - Issue2: what if there are no bridges in the network
 - Bridges from part of the shortest path between pairs of nodes in different paths in the network. We can utilize this characteristic of bridges
  - Find the edges that carry most of "traffic" in a network and successively remove edgesof high traffic. 

### Edge Betweenness
- lets assume 1 unit of 'flow' will pass over all shortest path btw any pair of nodes A and B.
- Betweenness of an edge is the total amount of flow it carries.
- If there are k sorted path between A and B, then 1/k units of flow will go along each shortest path. 
#### Girvan-Newman Algorithm
- repeat untill no edges are left:
 - calculate betweenness of edges
 - Remove edges with highest betweenness.

#### Clever way to compute Edge Betweenness
- Use Breadth-First search

''' python
for each node A:
    # Run BFS on A
    # Count the nubmer of shortest paths from A to any other node
    # Determine the amount of traffic from A to other nodes.
'''
- Consider the graph from the perspective of one node at atime
- Determine the amount of traffic from A to others

### Agglomerative methods
- start with each node representing their own cluster, then you start adding other nodes/merging the existing clusters together.

# LECTURE06
02-18-2015

## Guest Lecture Svitlana Volkova

## Social Media Data
- you can predict things about someone based on there internet posts 

## 2 approaches to collecting data
### Static (Batch) Predictions
- offline training
- Offline predictions
- Exploring 6 types of neighborhoods

### Streaming (Online) Inference
- Offline Training
- Relying on neighbor content
- Online predicitons in real time

# LECTURE07
02-23-2015

## Ideas tools and datasets

### Datasets

Tons of data sets from stanford
http://snap.stanford.edu/data/index.html

Yahoo answers
Advertising 
http://webscope.sandbox.yahoo.com/catalog.php
Common tags with urls

MOOC databases
student interaction throughout the course

USDA Dataset

Churny tweets People leaving some service 

Football (superbowl information)


word2vec - google developed program that tells you how related a word is to a set of other words
