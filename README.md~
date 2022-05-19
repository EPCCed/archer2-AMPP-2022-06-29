<img src="./images/Archer2_logo.png" width="355" height="100"
align="left"> <img src="./images/epcc_logo.jpg" align="right"
width="133" height="100">

<br /><br /><br /><br /><br />

# ARCHER 2 Advanced MPI course (July 2021)

[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

<h3>David Henty EPCC: 14 and 16 July 2021 09:30 - 17:00 BST, online</h3>

This course is aimed at programmers seeking to deepen their
understanding of MPI and explore some of its more recent and advanced
features. We cover topics including exploiting shared-memory access
from MPI programs, communicator management and neighbourhood
collectives. We also look at performance aspects such as which MPI
routines to use for scalability, MPI internal implementation issues
and overlapping communication and calculation.  Intended learning
outcomes

*  Understanding of how internal MPI implementation details affect performance
*  Techniques for overlapping communications and calculation
*  Knowledge of MPI memory models for RMA operations
*  Understanding of best practice for MPI+OpenMP programming
*  Familiarity with neighbourhood collective operations in MPI

<h3>Prerequisites</h3>

Attendees should be familiar with MPI programming in C, C++ or
Fortran, e.g. have attended the ARCHER2 MPI course.

<h3>Requirements</h3>

Participants must bring a laptop with a Mac, Linux, or Windows
operating system (not a tablet, Chromebook, etc.) that they have
administrative privileges on.

They are also required to abide by the [ARCHER2 Code of Conduct](https://www.archer2.ac.uk/about/policies/code-of-conduct.html).

<h3>Timetable (all times are in British Summer Time)</h3>

<p><blockquote>Unless otherwise indicated all material is Copyright
&copy; EPCC, The University of Edinburgh, and is only made available
for private study. </blockquote></p>

<h4>Day 1: Wednesday 14th July</h4>

 *   09:30 - 09:45 <a href="slides/L00-ARCHER2-PTC-Intro.pdf">ARCHER2 and PRACE training</a>
 *   09:45 - 10:15 <a href="https://b.socrative.com/login/student/">MPI Quiz</a> ("Room Name" is: **HPCQUIZ**)
 *   10:15 - 11:00 <a href="slides/MPI-Evolution.pdf">MPI History</a>
 *   11:00 - 11:30 Coffee
 *   11:30 - 13:00 <a href="slides/MPI-Internals.pdf">Point-to-point Performance</a>
 *   13:00 - 14:00 Lunch
 *   14:00 - 15:30 <a href="slides/MPI-Optimisation-ARCHER2.pdf">MPI Optimisations</a>
 *   15:30 - 16:00 Coffee
 *   16:00 - 17:00 <a href="slides/AMPP-Advanced-Collectives.pdf">Collectives</a>
 *   17:00 CLOSE

<h4>Day 2: Friday 16th July</h4>

 *   09:30 - 11:00 <a href="slides/L06-MPIandOpenMP.pdf">MPI + OpenMP (i)<a>
 *   11:00 - 11:30 Coffee
 *   11:30 - 13:00 MPI + OpenMP (ii) - *same slide deck as above*
 *   13:00 - 14:00 Lunch
 *   14:00 - 14:30 <a href="slides/IntroRMA.pdf">RMA Access in MPI</a>
 *   14:30 - 15:30 <a href="slides/SharedMemoryRMA.pdf">New MPI shared-memory model</a>
 *   15:30 - 16:00 Coffee
 *   16:00 - 17:00 Finish Exercises
 *   17:00 CLOSE

<h3>Exercise Material</h3>

<p><blockquote>Unless otherwise indicated all material is Copyright &copy; EPCC, The University of Edinburgh, and is only made available for private study. </blockquote></p>

<h4>Day 1</h4>

SLURM batch scripts are set to run in the short queue and should work any time. However, on days when the course is running, we have
special reserved queues to guarantee fast turnaround.

The reserved queue for today is called `ta033_186`. To use this queue, change the `--qos` and `--reservation` lines to:
````
#SBATCH --qos=standard
#SBATCH --reservation=ta033_186
````

 * <a href="exercises/ARCHER2-pingpong.pdf">Ping-pong exercise sheet</a>
 * <a href="https://github.com/EPCCed/archer2-AMPP-2021-07-14/raw/main/exercises/pingpong.tar">Ping-pong source code</a>
   
 * Description of 3D halo-swapping benchmark is in this <a href="https://github.com/davidhenty/halobench/">README</a>
 * Download the code directly to ARCHER2 using: `git clone https://github.com/davidhenty/halobench`
   - compile with `make -f makefile-archer2`
   - submit with `qsub archer2.job`
 * Other things you could do with the halo swapping benchmark:
   - change the buffer size to be very small ( a few tens of bytes) or very large (bigger than the eager limit) to see if that affects the results;
   - run on different numbers of nodes.
 * Note that you will need to change the number of repetitions to get reasonable runtimes: many more for smaller messages, many fewer for larger messages. Each test needs to run for at least a few seconds to give reliable results.
   
 * The collectives exercises are included in <a href="https://github.com/EPCCed/archer2-AMPP-2021-07-14/raw/main/exercises/collective.tar">this tar file</a>
   - instructions are included as comments at the top of each file
   - `mpigather.c` and `mpigather.f90` illustrate using vectors for gather operations;
   - `mpigather2d.c` and `mpigather2d.f90` extend to gathering a 2D array as described in the lectures;
   - solutions are include (e.g. `mpigathersol.c`);
   - there are also other codes that illustrate user-defined operations in reductions (not covered in this course).
 
<h4>Day 2</h4>

The reserved queue for today is called `ta033_187`. To use this queue, change the `--qos` and `--reservation` lines to:
````
#SBATCH --qos=standard
#SBATCH --reservation=ta033_187
````

 * <a href="exercises/traffic-advmpi.pdf">Traffic modeling exercise sheet</a>
 * <a href="https://github.com/EPCCed/archer2-AMPP-2021-07-14/raw/main/exercises/traffic.tar">Traffic model source code and solutions (MPI / OpenMP)</a>
   - note that the OpenMP Makefiles are not properly configured for ARCHER2. To
     compile correctly you need to change the following flags:
   - for the OpenMP C version: `CFLAGS= -O3 -fopenmp`
   - for the OpenMP Fortran version: `FFLAGS= -O3 -homp`
  * <a href="https://github.com/EPCCed/archer2-AMPP-2021-07-14/raw/main/exercises/traffic-RMA.tar">Traffic model source code and solutions (MPI RMA)</a>

---

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

