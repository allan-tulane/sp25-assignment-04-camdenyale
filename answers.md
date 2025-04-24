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


- **2b.**


- **2c.**

- **2d.**

- **2e.**



- **3a.**

   No a solution to MST is not guarenteed to be a solution to MMET. The MST minimizes the total weight of all the edges in the spanning tree, while MMET minimizes the maximum single edge weight. These can lead to different trees.

- **3b.**
  
  Using Kruskal's algorithm, sort the edges and find the most optimal solution. Then, iterate through each edge and find an MST without the current edge. Continue until all of the edges in MST have been iterated through, and the minimum weight difference of that edge is the second lowest weight. 

- **3c.**   
  The overall work is O(E log E) because MST dominates the runtime. 
