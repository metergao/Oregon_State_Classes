Project 5
====================
Project 5: Sockets and python

Due: Sunday, 8 December 23:59:59 -- NO LATE ASSIGNMENTS ACCEPTED

This project will require that you compute perfect numbers. These perfect numbers are numbers such that the sum of their proper divisors is equal to the number itself. For instance, the proper divisors of 6 are 1, 2, and 3, which sum to 6.

You will write 3 related programs to manage, report, and compute results. You are required to brute force the algorithm. Yes, this is ridiculous, but the algorithm is NOT the point of this assignment.

compute's job is to compute perfect numbers. It tests all numbers beginning from its starting point, subject to the constraints below. There may be more than one copy of compute running simultaneously.

manage's job is to maintain the results of compute. It also keeps track of the active compute processes, so that it can signal them to terminate, including the host name and performance characteristics.

report's job is to report on the perfect numbers found, the number tested, and the processes currently computing. If invoked with the "-k" switch, it also is used to inform the manage process to shut down computation. report will query the server for information, provide that to the caller, then shut down.

Use sockets for communication, with manage as the "master" process, or in other words, the server.

In order for the compute process to know what values to check, it will query the server for a range of values which it will check for perfect numbers. The server should send back a range that will take approximately 15 seconds for the client to check. In order for the server to know this, the clients must send some sort of information about their performance characteristics. To determine these performance characteristics (think FLOPS/IOPS), you will make use of a timing loop, where you execute a known number of operations, and time how long they take.

All processes should terminate cleanly on INTR, QUIT, and HANGUP signals. When the -k is flag is used on report, report sends an INTR to manage to force the same shutdown procedure. You will have to implement a standard to use via sockets to tell the other side to send itself the signal, via kill.

You will be implementing manage and report using python, while compute will be done in C. compute must utilize a separate thread or process for monitoring the control socket for a shut down message from the server.
You are required to use XML for data exchange. Further, you are not allowed to use any libraries to construct or parse the XML. You must implement this BY HAND.

Same collection of things to turn in as in previous assignments. Ensure that your write up includes a complete design, as well as a work log.

Please combine all of the above files into a bzipped tar ball prior to submission. There should be no directory hierarchy present in the tar ball, so that they extract to the current directory.
