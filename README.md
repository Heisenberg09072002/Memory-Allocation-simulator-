# Memory-Allocation-simulator-
Memory Allocation Sytem using c++ implemented using web dev
As we know, every process requires two types of time for its execution.
a) CPU time: Execution of process on CPU
b) I/O time: Time to access the input or output device
As Hard disk is Input and output device because CPU can read and write the data on
it. So, Process request to OS to access the hard disk. This time to access the hard
disk is called I/O time.
The method through which an OS decide, which request will be execute next is
called disk scheduling.
Disk scheduling algorithms are the algorithms that are used for scheduling a disk.
Generally, the scheduling refers to a time-table for completing any task or a job.
With the help of the operating system, disk scheduling is performed. We use disk
scheduling to schedule the Input/output requests that arrive for the disk. Disk
Scheduling is also called Input/output scheduling.
Goals of Disk Scheduling Algorithms
o Fairness
o High throughout
o Minimal traveling R/W head time
1.FCFS (First Come First Serve) Algorithm
This algorithm entertains requests in the order they arrive in the disk queue.
It is the simplest disk scheduling algorithm.
The algorithm looks very fair but generally, it does not provide the fastest service.
Advantage:
1. It is the easiest algorithm to implement and understand.
2. As all processes are addressed one at a time, starvation is avoided.
Disadvantage:
1. As only one process is addressed at a time, the total seek time is huge.
2. The algorithm is overall inefficient.
2.SSTF (Shortest Seek Time First) Algorithm
This algorithm services that request next which requires least number of
head movements from its current position regardless of the direction.
It breaks the tie in the direction of head movement.
Advantage:
1. The seek time is lower as compared to FCFS.
2. SSTF provides an increased throughp
Disadvantage:
1. Finding out the closest request causes an overhead which could otherwise be
avoided.
2. Process requests which are further away from the head can end up starved
for the CPU.
3. It provides high variance in response time and waiting time.
4. Changing the direction of the head so frequently adds extra time to the
algorithm.
3.SCAN Algorithm
This algorithm scans all the cylinders of the disk back and forth.
Head starts from one end of the disk and move towards the other end servicing all
the requests in between.
After reaching the other end, head reverses its direction and move towards the
starting end servicing all the requests in between.
SCAN Algorithm is also called as Elevator Algorithm.
Advantages:
1. SCAN is a simple, easy to implement algorithm.
2. It does not lead to starvation.
3. The variance in response time and waiting time is comparatively lower.
Disadvantages:
1. It causes long waiting time for the cylinders just visited by the head.
2. As the head is made to move till the end of the disk even if there are no more
requests to be serviced, the overall time taken is increased.
4.C-SCAN (Circular-SCAN) Algorithm
Circular-SCAN Algorithm is an improved version of the SCAN Algorithm.
Head starts from one end of the disk and move towards the other end servicing all
the requests in between.
After reaching the other end, head reverses its direction. It then returns to the
starting end without servicing any request in between.
Advantages:
1. The waiting time for the cylinders just visited by the head is reduced as
compared to the SCAN Algorithm.
2. It provides uniform waiting time.
3. It provides better response time.
Disadvantages:
1. It causes more seek movements as compared to SCAN Algorithm.
2. As the head is moved till the end of the disk even if there are no more
requests to be serviced, time taken is increased unnecessarily.
5.LOOK Algorithm
LOOK Algorithm is an improved version of the SCAN Algorithm.
Head starts from the first request at one end of the disk and moves towards the last
request at the other end servicing all the requests in between.
After reaching the last request at the other end, head reverses its direction. It then
returns to the first request at the starting end servicing all the requests in between.
Advantages:
1. The head is not made to move till the ends of the disk when there are no
more requests to be serviced.
2. Considerably better performance is observed when compared to SCAN.
3. It does not lead to starvation.
4. The variance in response time and waiting time is very low.
Disadvantages:
1. Finding the end requests leads to an overhead.
2. It causes long waiting time for the cylinders just visited by the head.
6.C-LOOK Algorithm
Circular-LOOK Algorithm is an improved version of the LOOK Algorithm.
Head starts from the first request at one end of the disk and moves towards the last
request at the other end servicing all the requests in between.
After reaching the last request at the other end, head reverses its direction. It then
returns to the first request at the starting end without servicing any request in
between.
Advantages:
1. It does not make the head to move till the ends of the disk when there are no
more requests to be serviced.
2. The waiting time for the cylinders just visited by the head is reduced.
3. It provides better performance as compared to LOOK Algorithm.
Disadvantage:
1. Finding the end requests leads to an overhead
