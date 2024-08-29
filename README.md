Algorithm: Plotting Time Complexity in C Using Gnuplot
1. Implement Sorting Algorithms:
o Write C functions for Bubble Sort, Insertion Sort, and Selection Sort.
o Ensure all three functions are defined in the same program.
2. Generate Data for Time Complexity:
o Create an array of integers of varying sizes (e.g., 100, 200, 500, 1000, etc.).
o For each array size:
 Generate a random array of integers.
 Measure the time taken by each sorting algorithm to sort the array.
 Record the array size and corresponding time taken in a data file.

3. Measure Execution Time:
o Use the clock() function from time.h to measure the start and end time of
each sorting function.
o Calculate the time difference to determine the execution time.
4. Store Results in a File:
o For each array size, save the time taken by each algorithm in a text file in the
format:
mathematica
Copy code
Array Size Bubble Sort Time Insertion Sort Time Selection
Sort Time
100 0.001 0.002 0.0015
200 0.004 0.005 0.0035
...

5. Plot the Graph Using Gnuplot:
o Open Gnuplot.
o Load the data file created in the previous step.
o Plot the graph with Array Size on the x-axis and Time on the y-axis, with
separate lines for each sorting algorithm.

Detailed Algorithm
1. Implement Sorting Functions:
o Write the C functions for each sorting algorithm.
2. Setup the Program:
o Include necessary libraries: stdio.h, stdlib.h, time.h.
o Create the main function.
o Declare an array and fill it with random integers.
3. Measure and Record Time:
o Use a loop to vary the size of the array.
o For each size:
 Copy the original array to avoid sorting an already sorted array.

 Measure the time taken by Bubble Sort, Insertion Sort, and Selection
Sort.
 Store the size and corresponding times in a text file.

4. Plotting Using Gnuplot:
o After running the C program, open the terminal and start Gnuplot.
o Use the plot command in Gnuplot to visualize the data.
o Example Gnuplot command:
csharp
Copy code
plot &quot;data.txt&quot; using 1:2 with lines title &#39;Bubble Sort&#39;, \
&quot;data.txt&quot; using 1:3 with lines title &#39;Insertion Sort&#39;, \
&quot;data.txt&quot; using 1:4 with lines title &#39;Selection Sort&#39;
o This command plots the time complexities of the three algorithms on the same
graph.

This algorithm provides a structured approach to solving the problem, helping to understand
the steps involved in both coding the sorting algorithms and visualizing their time
complexities using Gnuplot.
