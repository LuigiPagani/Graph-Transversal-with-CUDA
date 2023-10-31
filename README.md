# Graph Transversal with CUDA: Breadth-First Search (BFS)

This repository provides an efficient implementation of the Breadth-First Search (BFS) algorithm using CUDA for parallel computing on GPUs. The BFS algorithm is applied to a randomly generated graph, represented as an adjacency matrix.

## Contents

- `main.cu`: This is the main CUDA C source file that contains the BFS algorithm implementation and the kernel invocations.

## Implementation

The code utilizes both global queuing and block queuing techniques to manage parallelism in BFS. The implementation comprises two kernels - one for global queuing (`gpu_global_queuing_kernel`) and one for block queuing (`gpu_block_queuing_kernel`). The `GraphBFS` function orchestrates the BFS process, which continues until all nodes have been visited. The main function (`main`) generates a random graph, executes the BFS, and measures the execution time.

## Building the Project

1. Navigate to the source directory.
2. Compile the code using the following command:

```bash
nvcc main.cu -o bfs
```

## Running the Project

Execute the compiled code with the following command:

```bash
./bfs
```

## Output

The program outputs the time taken for the BFS operation in seconds.

## Requirements

Please ensure that the CUDA toolkit is installed and correctly configured on your system.

## License

This project is licensed under the MIT License.
```
