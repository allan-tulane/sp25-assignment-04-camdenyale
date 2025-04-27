# CMPS 2200 Assignment 5
## Answers

**Name:**   Camden Yale






- **1a.**

  $\log_d n$

- **1b.**
  
  delete-min: O(d $\log_d n$), minimum number of node d's children

  insert: O($\log_d n$), only swap the parent of each node

- **1c.**
  
  $m$ = |E| and $n$ = |V|   

  $m$ deletes while $n$ inserts   

  Therefore, O($nd\log_d n$ + $m\log_d n$)
- **1d.**

  d = |E| / |V|  

- **2a.**   
  APSP(i, j, 0):
  
    APSP(0,0,0) = 0
  
    APSP(0,1,0) = -2
  
    APSP(0,2,0) = 2
  
    APSP(1,0,0) = $\infty$
  
    APSP(1,1,0) = 0
  
    APSP(1,2,0) = 0
  
    APSP(2,0,0) = 0
  
    APSP(2,1,0) = 0
  
    APSP(2,2,0) = 0

  APSP(i, j, 1):
  
    APSP(0,0,1) = 0
  
    APSP(0,1,1) = -2
  
    APSP(0,2,1) = -1
  
    APSP(1,0,1) = $\infty$
  
    APSP(1,1,1) = 0
  
    APSP(1,2,1) = 1
  
    APSP(2,0,1) = $\infty$
  
    APSP(2,1,1) = $\infty$
  
    APSP(2,2,1) = 0

  APSP(i, j, 2):
  
    APSP(0,0,2) = 0
  
    APSP(0,1,2) = -2
  
    APSP(0,2,2) = -1
  
    APSP(1,0,2) = $\infty$
  
    APSP(1,1,2) = 0
  
    APSP(1,2,2) = 1
  
    APSP(2,0,2) = $\infty$
  
    APSP(2,1,2) = $\infty$
  
    APSP(2,2,2) = 0


- **2b.**

  APSP(i, j, 2) = min(APSP(i, j, 1), APSP(i, 2, 1) + APSP(2, j, 1))


- **2c.**

  Shortest path from i to j would be either the best path without using k, or the path going through k.
  
  Therefore, APSP(i, j, k) = min(APSP(i, j, k - 1), APSP(i, k, k - 1) + APSP(k, j, k - 1))

- **2d.**

  The number of distinct subproblems is n * n * n = $n^3$.

  Therefore, the work is O($n^3$)

- **2e.**

  Our algorithm is preferable when the graphs are smaller and more dense. 

- **3a.**

   No a solution to MST is not guarenteed to be a solution to MMET. The MST minimizes the total weight of all the edges in the spanning tree, while MMET minimizes the maximum single edge weight. These can lead to different trees.

- **3b.**
  
  Using Kruskal's algorithm, sort the edges and find the most optimal solution. Then, iterate through each edge and find an MST without the current edge. Continue until all of the edges in MST have been iterated through, and the minimum weight difference of that edge is the second lowest weight. 

- **3c.**   
  The overall work is O(E log E) because MST dominates the runtime. 
