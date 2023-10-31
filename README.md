# Graph-Transversal-with-CUDA

# BFS-CUDA  
   
This repository contains an efficient implementation of the Breadth-First Search (BFS) algorithm using CUDA for parallel computing on GPUs. The BFS algorithm is applied on a randomly generated graph, represented as an adjacency matrix.   
  
## Files  
   
`main.cu` - The main CUDA C source file that contains the BFS algorithm implementation and the kernel invocations.  
   
## Implementation Details  
   
The code makes use of both global queuing and block queuing techniques to handle parallelism in BFS. The implementation includes two kernels - one for global queuing (`gpu_global_queuing_kernel`) and one for block queuing (`gpu_block_queuing_kernel`). The `GraphBFS` function controls the BFS process, which runs until all nodes have been visited. The main function (`main`) generates a random graph, runs the BFS, and measures the time it takes.  
   
## Compilation  
   
To compile the code, navigate to the source directory and run the following command:  
   
```  
nvcc main.cu -o bfs  
```  
   
## Execution  
   
To run the compiled code, use the following command:  
   
```  
./bfs  
```  
   
## Output  
   
The program will print the time elapsed for the BFS operation in seconds.  
   
## Note  
   
The code assumes that the CUDA toolkit is installed and correctly configured on the system.  
   
## License  
   
This project is licensed under the MIT License.
