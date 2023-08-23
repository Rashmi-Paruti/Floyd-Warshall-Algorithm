# Floyd-Warshall-Algorithm
• It is used to solve All Pairs Shortest Path Problem.

• It computes the shortest path between every pair of vertices of the given graph.

• Floyd Warshall Algorithm is an example of dynamic programming approach.

# Advantages
• It is extremely simple.

• It is easy to implement

# Algorithm
Create a |V| x |V| matrix // It represents the distance between every pair of vertices as given

For each cell (i,j) in M do- 

if i = = j

M[i][j] = 0 // For all diagonal elements, value = 0

if (i , j) is an edge in E

M[i][j] = weight(i,j) // If there exists a direct edge between the vertices, value = weight of edge

else

M[i][j] = infinity // If there is no direct edge between the vertices, value = ∞

for k from 1 to |V|

for i from 1 to |V|

for j from 1 to |V|

if M[i][j] > M[i][k] + M[k][j]
M[i][j] = M[i][k] + M[k][j]

# Time Complexity-
• Floyd Warshall Algorithm consists of three loops over all the nodes.

• The inner most loop consists of only constant complexity operations.

• Hence, the asymptotic complexity of Floyd Warshall algorithm is O(n3).
