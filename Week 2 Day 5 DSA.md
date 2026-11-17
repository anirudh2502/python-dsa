# Week 2 Day 5 DSA  
  
## ++Day 5++  
  
## ++Graph++:  
It is a non-linear data structure consisting of vertices (V) and edges (E).  
* **++Vertices (V)++** -  
- Fundamental units of a graph   
- Also known as vertex/node  
- They can be labelled/unlabelled   
  
* **++Edges (E)++** -   
- Used to connect two nodes of a graph in any possible way  
- Also known as arcs  
- They can be labelled/unlabelled  
- Can be ordered pair of nodes in a directed graph  
  
  
  
## ++Directed v/s undirected graphs++:  
![Directed Graph](Attachments/54146670-8452-4E6A-AFCD-451710B31292.png)  

| Directed | Undirected  |
| ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| Provides a clear representation of relationships with direction | Simple to understand and manipulate  |
| Has no symmetry (A -> B != B -> A)                                                        | It has symmetry (A -> B == B -> A)                                                    |
| May require more memory because of storing direction | Requires less memory, hence more memory-efficient |
| Suitable for modelling workflows  | Provides limited modelling capability for directed relationships  |
| Traversal is more complex due to direction  | Traversal is simple because no direction check is needed |
| It is easy to represent one-direction scenarios  | It is difficult to represent specific scenarios with one-way relations |
  
  
  
## ++Weighted v/s unweighted graphs++:  

| Weighted  | Unweighted  |
| -------------------------------------------------------------------- | ------------------------------------------------------------------ |
| Provides a clear representation of relationships with cost/magnitude | Simple to understand and manipulate |
| Edges carry numerical values  | Edges carry no values, all connections are equal  |
| Required more memory because of storing a weight per edge  | Requires less memory, hence more memory-efficient  |
| Suitable for modelling costs, distances, time, capacity | Provides limited modelling capability  |
| Focus is on optimisation | Focus is on connectivity  |
| Traversal is complex due to weight comparison  | Traversal is simple because no weight check is needed |
| Easy to represent real-world scenarios like GPS road maps | Difficult to represent scenarios where connections differ in costs |
  
  
  
  
## ++Adjacency matrices and Adjacency lists :++  

| Adjacency matrices | Adjacency lists |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| Storage: O(V^2). Uses a full grid  | Storage: O(V + E). Stores only real connections                              |
| Add vertex: O(V^2). Make a bigger grid and copy everything | Add vertex: O(1). Just add one new entry  |
| Add edge: O(1). Set matrix[i][j] = 1                                                     | Add edge: O(1). Add to the end of the list  |
| Remove vertex: O(V^2). Make a smaller grid and copy everything | Remove vertex: O(V + E). Find it, then remove its connections |
| Remove edge: O(1). Set matrix[i][j] = 0 | Remove edge: O(E). Search for it, then delete |
| Query edge: O(1). Check matrix[i][j] | Query edge: O(V). Scan the neighbours of vertex i  |
  
  
  
  
## ++Disconnected graphs++:   
It is an undirected or directed graph where at least one pair of vertices has no path connecting them, meaning the graph is split into two or more isolated connected components.   
![Disconnected Graph](Attachments/A2E89914-C036-4CBB-9AE2-0173EA754071.png)  
