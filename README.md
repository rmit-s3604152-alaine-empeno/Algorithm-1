## Background
You may of heard of the phrase, �six degrees of separation�, but did you know where it came from?
It is based on the idea that anyone in the world is more or less separated from anyone else in the
world by 6 direct acquaintances, i.e., you know someone who knows someone who knows someone ...
Although the phrase is often incorrectly attributed to American psychologist Milgram and a few others,
nevertheless, it is of interest to understand the set of experiments that popularised the phrase. In
1967, Milgram setup an experiment to test the small world phenomena (everyone is linked to everyone
else via a short chain of acquaintances). He gave around 300 volunteers a name of someone in the US
and instructions to send the letter to the person if they know them, or if they don�t, to send the letter
an acquaintance that they think would know this person. Before sending on the letter, they should
record their name in a roster and send this with the letter. If the letter get to the target person, this
person is asked to send the roster, now containing the chain of persons, back to Milgram. Analysing
the rosters that came back, he found on average, it took a chain of about 6 persons to reach the target
people, which lead to the term of �six degrees of separation�.
This problem can be studied in terms of graphs, specifically social networks modelled as graphs.
The vertices in such a graph represent people and edges represent relationships. There are many 
types of social networks, in this program. In a friendship graph, the edges are undirected 1 and represent friendship. 
The separation between a pair of persons can be measured by the shortest path distance between their respective vertices, and we can replicate
Milgram�s experiment by calculating the average shortest path distance between all pairs of vertices
(representing people).
The adjacency list and adjacency graph representations. The performance of each representation varies 
depending on the characteristics of the graph. In this program, I will implement both representations, 
and evaluate how well they perform when representing a friendship graph and computing the average separation between a pair
of people.

## Description
Implement the undirected graph using the adjacency list and adjacency matrix
representations. Each representations will be implemented by a data structure. 
- Create an empty undirected graph.
- Add a vertex to the graph.
- Add an edge to the graph.
- Neighbours of a vertex in the graph.
- Remove a vertex from the graph.
- Remove an edge from the graph.
- Print out the set of vertices of the graph.
- Print out the set of edges of the graph.
- Compute the shortest path between a pair of vertices in the graph.

## Data Structure Details
Graphs can be implemented using a number of data structures. I have implement the graph
abstract data type using the following data structures:
- Adjacency list, using an array of linked lists.
- Adjacency matrix, using a 2D array (an array of arrays).

## Operations Details
Operations to perform on the implemented graph abstract data type are specified on the command
line. They are in the following format:
```
<operation> [arguments]
```
where operation is one of {AV, AE, N, RV, RE, V, E, S, Q} and arguments is for optional arguments
of some of the operations. The operations take the following form:

add a vertex with label �vertLabel� into the graph.
```
- AV <vertLabel> 
```

add an edge with source vertex �srcLabel� and target vertex
�tarLabel� into the graph.
```
- AE <srcLabel> <tarLabel>
```

Return a set of neighbours for vertex �vertLabel�. The ordering of the neighbours
does not matter. See below for the required format.
```
- N <vertLabel>
```

remove vertex �vertLabel� from the graph.
```
- RV <vertLabel> 
```

remove edge with source vertex �srcLabel� and target vertex �tarLabel�
from the graph.
```
- RE <srcLabel> <tarLabel>
```

prints the vertex set of the graph. See below for the required format. The vertices can be
printed in any order.
```
- V 
```

prints the edge set of the graph. See below for the required format. The edges can be printed
in any order.
```
- E 
```

compute the shortest path distance between vertex �vertLabel1�
and vertex �vertLabel2�. If there is no path between the two vertices, then their distance
is -1. See below for the required format.
```
- S <vertLabel1> <vertLabel2> 
```

quits the program
```
- Q 
```
