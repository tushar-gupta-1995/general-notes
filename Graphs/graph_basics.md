# What is a graph:
A graph is an object with the following three sets as attributes:
- vertices:  the smallest unit of a graph, represents a unique and atomic unit.
- edges: edge describes the relation between vertices. edges must have a source and destination, if source and destination is same, it is as self looped edge.
- incidence function: incidence function is just assigning a vertices to the edges.

# REMEMBER:  a graph has no relevant shape, as long as i do not change the number of vertices,edges and their incidence function, i can rearrange the vertices or their edges but the graph still remains the same.

# aliases of graph
complete graphs are prefixed with k followed by number of vertices.
Refer the below images
![complete graphs](Graphs/images/graph_types.png)

# Connected graph(undirected):
For any two pair of vertices in the graph, there is a path that connects them. The path can span multiple other vertices, but should exist for graph to be connected.

# Complete graph:
For any two pair of vertices there exists a direct edge that should not span any third vertex, if there are n vertices, chose any 2, and there is a unique edge, thus the number of edges is nc2.

# Planer Graph
a graph which can be drawn on a 2d plane such that no 2 edges cross each other.
Note: since the shape of the graph is irrelevant, as long as vertices,edges and their relationship(incidence function), we need to find
just one orientation of the graph where no 2 edges cross each other.
Therefore k4 whose default orientation(a square with 2 diagonals) seems a non planer, is actually planer.
## TODO: Try drawing it on a copy and attach k4 here.




