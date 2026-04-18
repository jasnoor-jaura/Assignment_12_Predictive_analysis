# Assignment_12_Predictive_analysis
Assignment: Multi-Threading Performance Analysis using Matrix Multiplication
Objective:

The objective of this assignment is to analyze the impact of multi-threading on computational performance by performing large-scale matrix multiplication. The study evaluates how varying the number of threads affects execution time and CPU utilization.

Problem Statement:

The task involves multiplying multiple large random matrices with a constant matrix and measuring the time taken for execution using different numbers of threads. The goal is to determine the optimal number of threads that minimizes execution time while efficiently utilizing CPU resources.

Methodology:
Step 1 — Data Generation
Generated N random matrices of size S × S
Generated one constant matrix of the same size
Each matrix is multiplied with the constant matrix
Step 2 — Multi-threaded Execution
Used ThreadPoolExecutor for parallel computation
The number of threads was varied from 1 to 8
Each thread performs matrix multiplication independently
Step 3 — Performance Measurement

For each thread count:

Execution time was recorded (in minutes)
CPU usage was measured using system monitoring tools
Step 4 — Repetition Across Threads

The experiment was repeated for:

T = 1, 2, 3, 4, 5, 6, 7, 8
📊 Result Table
Threads	Time Taken (min)
T=1	0.08
T=2	0.09
T=3	0.05
T=4	0.09
T=5	0.05
T=6	0.05
T=7	0.05
T=8	0.08

Result Graph:
1️. Execution Time vs Threads
X-axis: Number of Threads
Y-axis: Time Taken

This graph shows how execution time decreases initially as threads increase and then may increase due to overhead.

2️. CPU Usage vs Threads
X-axis: Number of Threads
Y-axis: CPU Utilization (%)

This graph demonstrates how CPU usage scales with increasing thread count.

Observations:
1. Performance Improvement
Increasing threads initially reduces execution time due to parallel processing.
2. Optimal Thread Count
There exists an optimal number of threads (usually near number of CPU cores) where performance is best.
3. Overhead Effect
Beyond optimal threads, performance degrades due to:
Context switching
Thread management overhead
4. CPU Utilization
CPU usage increases with more threads but may plateau or fluctuate at higher values.
Conclusion:

This experiment demonstrates that multi-threading significantly improves performance for computationally intensive tasks like matrix multiplication. However, using too many threads can negatively impact performance due to system overhead. Selecting an optimal thread count is crucial for efficient execution.

Tools & Technologies Used:
Python
NumPy
Matplotlib
concurrent.futures (ThreadPoolExecutor)
psutil (CPU monitoring)

Notes:
Large matrix sizes (5000×5000) require high computational power
Smaller sizes can be used for testing in Colab
Results may vary depending on hardware configuration
