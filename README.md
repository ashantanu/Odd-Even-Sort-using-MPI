Implement Odd Even sort using MPI.

What is Odd Even sort?

The odd-even transposition algorithm sorts n elements in n phases (n is even), each of which requiresn/2 compare-exchange
operations. This algorithm alternates between two phases, called the odd and even phases. Let <a 1, a 2, ..., an > be the sequence to be sorted. During the odd phase, elements with odd indices are compared with their right neighbors, and if they are out of sequence they are exchanged; thus, the pairs (a 1, a2), (a3, a 4), ..., (an-1, an ) are compare-exchanged (assuming n is even). Similarly, during the even phase,elements with even indices are compared with their right neighbors, and if they are out of sequence they are exchanged; thus, the pairs (a2, a 3), (a 4, a5), ..., (an-2, an-1) are compare-exchanged. After n phases of odd-even exchanges, the sequence is sorted. Each phase of 2 the algorithm (either odd or even) requires Q(n) comparisons, and there are a total of n phases; thus, the sequential complexity isQ(n^2 ).
(Source:Introduction to Parallel Computing-Ananth Gramma)



How to execute?

type the following commands in the terminal-

mpic++ oddEven.cpp

mpirun -np [number of processors] a.out
