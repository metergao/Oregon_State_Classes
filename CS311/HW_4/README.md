Project 4
====================
Homework 4: Threads and shared memory

Due 26 November 2013, 23:59:59

For this project, you will be required to find all prime numbers within the range of a 32 bit unsigned integer. There are some specific requirements for the purposes of this project:

You will be writing 2 slightly different versions of this project
	1.A threaded version with implicit sharing

	2.A version using multiple processes and shared memory

You are required to thread your program using the pthreads library.

You are required to make use of a bitmap, which will be used to store the results of your checking. For the threaded version, this will be in the heap, for shared memory it must be located in the shared memory object.

You CAN NOT brute force this algorithm. You must use a more sophisticated method for obtaining the list of prime numbers. The Sieve of Eratosthenes was given as the first assignment in this class.

If you are attached to a specific method, or are a mathematician with an interest in number theory, feel free to use other methods.

After obtaining your list of primes, determine whether the prime is happy or sad:
	Starting with any positive integer, replace the number by the sum of the squares of its digits, and repeat 		the process until the number equals 1 (where it will stay), or it loops endlessly in a cycle which does 	not include 1. Those numbers for which this process ends in 1 are happy numbers, while those that do not 		end in 1 are sad numbers.

This part should also be done in parallel, using both methods.

Just as in the last assignment, you are required for your processes to handle signals. I don't require that you handle signals in your threaded program, but extra credit will be given if you do.

Please provide timings based on the number of threads or processes. Also, for extra credit, also vary the max value you are considering. Keep in mind this will require some form of multi-dimensional plot. These timings should be plotted in a fashion that makes sense, and included in your writeup of the project. Please plot both versions on the same plot, in order to provide a comparison.

Your writeup should include a program design and/or flow chart, a work log, timings, and a discussion of why you implemented the code in the fashion that you chose. Essentially, you will be providing a justification for design decisions, and a discussion of any interesting or frustrating aspects of the project, as well as any places where you had to deviate from your design. It is highly recommended that you document your design in a separate file that can be timestamped, or submit it to a repository. In other words, do the design apriori, rather than ex post facto. Don't forget to include documentation for both the code and the solution you are creating.

To give you something to shoot for, I have serial code which generates all the primes requested in under 45 seconds. Beat this time, and receive extra credit. This is strictly the prime generation time, rather than the happiness checking.

Things to turn in:
	1.C source code for the solutions to the posed problem.
	2.A makefile to build your code
	3.A writeup of your project, including work log, as described above.

Please combine all of the above files into a bzipped tar ball prior to submission. There should be no directory hierarchy present in the tar ball, so that they extract to the current directory.
