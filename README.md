--> simple-Multi-threading
This C++ program demonstrates parallel programming by utilizing multi-threading for matrix and vector operations.It employs lambda functions to define thread tasks and executes them concurrently to illustrate parallelization concepts. Additionally, the program records and compares execution times, highlighting the performance benefits of threading.
# Parallel Programming with Threads in C++

This project demonstrates **parallel programming** in C++ using **multi-threading** for both matrix and vector operations.  
It leverages **lambda functions** to define thread tasks, executes them concurrently, and records execution times to highlight the performance benefits of parallelization.

---

## Features

- Parallel execution of **matrix operations** using threads.  
- Parallel execution of **vector operations** using threads.  
- **Lambda functions** for capturing variables and passing custom logic to threads.  
- Measurement of execution times to compare performance.  
- Demonstrates concepts of thread arguments, synchronization, and workload distribution.

---

## Implementation Details

### Global Variables
- `long long t_time`: Accumulates the total execution time across intervals.  
- `int thread_cnt`: Stores the number of threads used during execution.  

### Functions

#### Matrix Problem
- **`thread_args1`**: Structure for passing parameters to matrix-related threads.  
- **`thread_func1`**: Thread function to perform matrix operations.  
- **`parallel_for`**: Divides the matrix into chunks, executes the given lambda in parallel, and records execution time.  

#### Vector Problem
- **`thread_args`**: Structure for passing parameters to vector-related threads.  
- **`thread_func`**: Thread function to perform vector operations.  
- **`parallel_for`**: Divides the vector into chunks, executes the given lambda in parallel, and records execution time.  

#### Main Function
- Calls `user_main` (can be replaced with custom logic).  
- Uses **lambda expressions** to demonstrate capturing variables by value and reference.  
- Executes both **matrix** and **vector** parallel operations.  
- Prints the total execution time.  

---

## 📌 Example Lambda Usage
```cpp
auto lambda_val = [=]() { /* captures by value */ };
auto lambda_ref = [&]() { /* captures by reference */ };
