# Ford-Fulkerson Algorithm (Max Flow)

This repository contains an implementation of the **Ford-Fulkerson algorithm** for computing the **maximum flow in a flow network**.  
The project includes both a clean version of the algorithm and a debug version that prints augmenting paths, residual graphs, and saturated edges for better understanding.  

## Files in this Repository
- **`max_flow.cpp`** → Standard Ford-Fulkerson implementation.  
- **`max_flow_debug.cpp`** → Debug version showing detailed steps (augmenting paths, residual graph states, and saturated edges).  
- **`input.txt`** → Example graph input file used for testing.  

## Input Format
The graph is given in the form of an adjacency matrix in `input.txt`.  

Example (`input.txt`):  
6
0 16 13 0 0 0
0 0 10 12 0 0
0 4 0 0 14 0
0 0 9 0 0 20
0 0 0 7 0 4
0 0 0 0 0 0

- First line → number of vertices (e.g., `6`).  
- Next lines → adjacency matrix of the graph where `graph[u][v]` is the capacity of edge `u → v`.  

## ⚙️ How to Compile & Run
### Compile
```bash
g++ -std=c++17 -O2 -o max_flow.exe max_flow.cpp
g++ -std=c++17 -O2 -o max_flow_debug.exe max_flow_debug.cpp
Get-Content input.txt | .\max_flow.exe
Get-Content input.txt | .\max_flow_debug.exe
Augmenting Path: 0 1 3 5 
Residual Graph:
0 -> 1 | cap: 4
0 -> 2 | cap: 13
...
Final Max Flow = 19
Saturated edges:
1 -> 3 | fully used (cap 12)
4 -> 3 | fully used (cap 7)
[max_flow_debug.cpp](https://github.com/user-attachments/files/22086883/max_flow_debug.cpp)
[max_flow.cpp](https://github.com/user-attachments/files/22086880/max_flow.cpp)
[input.txt](https://github.com/user-attachments/files/22086874/input.txt)

Learning Process
This project was created to:
Practice implementing Graph Algorithms in C++.
Understand how maximum flow problems work.
Visualize the step-by-step execution of Ford-Fulkerson with the debug version.

Future Improvements
Add support for larger test cases.
Implement Edmonds-Karp (BFS version of Ford-Fulkerson).
Add visualization for residual graph using Python/Graphviz.

---
