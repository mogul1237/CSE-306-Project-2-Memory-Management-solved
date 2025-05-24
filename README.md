# CSE-306-Project-2-Memory-Management-solved

Download Here: [CSE-306 Project 2 – Memory Management solved](https://jarviscodinghub.com/assignment/project-2-memory-management-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

What to do. Implement the Memory module of OSP2.
The project files are found on the Blackboard in the Assignments section.
Details of what you are supposed to do are given in the OSP2 manual (the chapter on memory
management). The additional requirements are:
1. You have to implement a modified 2-handed clock (M2HC) page replacement algorithm
similar to (but not exactly) the one described on pages 380-381 in the textbook. You also
have to use the dirty-bit optimization (if you do not optimize for clean frames, OSP2 issues
warnings, which is not OK and you will lose points).
2. The M2HC page replacement algorithm works as follows.
(a) The first hand, called the cleaner, sweeps all eligible (for replacement) frames1 at
regular intervals of 4000 clock ticks and sets the use bits of these frames to 0.2 To
arrange for an asynchronous process to run at regular intervals, use the OSP2 feature
called daemon. Read about daemons in the OSP2 manual.
(b) At page faults, if no free frame is available, the second hand, called the chooser, sweeps
the eligible frames and selects one with the use bit of 0 for replacement. If no such
frame exists, choose some eligible frame at will.
(c) In addition, the daemon (that runs on behalf of the cleaner hand) should swap out
approximately every 10th dirty page it finds.
Your objective in this project is to get your implementation to run under OSP2 without errors
and warnings with the parameter files that appear in the Misc subdirectory (the files with the
.osp extension). As explained earlier, occasional errors (every 7-10th run) should not be a cause
of concern, if they are unrelated to memory management.
1 You have to figure out which pages are eligible based on your studying of the subject of memory management.
2 You should be able to use the referenced flag of OSP2 frames as the use bit. Or create your own.
1
Statistics. Compare and explain your statistics with respect to those produced by Demo.jar.
(Demo.jar uses a very simplistic algorithm for page replacement: it scans the entire frame table
and chooses the first replaceable frame.) The statistics of interest are:
• The number of pages swapped in and out
• CPU utilization
• Service time per thread (avg turnaround time)
• Normalized service time per thread (avg normalized turnaround time)
These statistics are part of the snapshots in the file OSP.log, which is produced during the runs.
The meaning of these statistics is explained both in the textbook and in the OSP2 manual.
Important notice on the use of Git. You must use Git to maintain your project files and
you must make frequent commits to your repository. The Git repository must be in Github
classroom. Follow this link to create a repository in this course’s classroom for Project 2:
After a few clicks you will get a repository named cse306-project-2-YourGuthubId. The repository will automatically become private and you should not attempt to change that. Note: this
repository is different from that of Project 1.
We will be checking your repository and your commit logs to make sure that substantial
activity has been taking place over a period of time. If there are less than 5 nontrivial commits,
significant penalty will apply. Other than that, same requirements to your code as in Project 1.
How to submit. Zip-up your main branch and submit the zip file via Blackboard. Github
has a button for that: Clone or download/Download ZIP. Normally, the zip file will have a top
folder with a name like cse306-project-2-YourGuthubId-master, but if not then make sure
that your submitted zip file has a top folder with such a name. Do not forget to include your
name and Student Id in the program source-files. Do not submit paper-based material.
This project is to be done individually. Each source file must include the following pledge:
I pledge my honor that all parts of this project were done by me individually, without collaboration with anyone, and without consulting external
sources that help with similar projects.
