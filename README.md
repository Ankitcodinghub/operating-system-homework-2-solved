# operating-system-homework-2-solved
**TO GET THIS SOLUTION VISIT:** [Operating-System Homework 2 Solved](https://www.ankitcodinghub.com/product/operating-system-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;110241&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Operating-System Homework 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Objectives

• Multi-threaded Program

• Take advantage of multi-core systems

• Load sharing

• Linux Kernel Module

• Understand how to write a kernel module

• Understand how to provide read/write operations of proc files to users

Overall Flow

1. The kernel module creates a proc entry/file

2. The multithreaded program does the matrix multiplication

3. Each thread writes its thread ID to the proc entry

4. The kernel module gets and records the runtime and context switch times of the thread

5. The multithreaded program reads the proc entry to get the runtime and context switch information

6. The multithreaded program displays the information on the console

Requirement – Kernel Module

1. You have to write a kernel module named My_proc

2. The kernel module has to create a proc file with pathname

/proc/thread_info during its initialization/loading

3. You have to implement file operations of the proc file

a) User threads will write their thread ids to the proc file. When a user thread writes its id, the kernel module should record the thread id, get the thread execution time and context switch count of the thread.

*Note: thread execution time can be obtained from utime, and context switch count = nvcsw + nivcsw, where utime, nvcsw and nivcsw are fields of a task structure.

b) When the proc file is read, the thread relationships and the above timing information of all the recorded threads should be output to the reader.

Refer to Reference 4 for kernel module programming!

1. You need to write a multithreaded program to perform matrix multiplication.

2. The program starts with a single main/parent thread, which is responsible for creating multiple

worker threads.

3. Each worker thread should perform a part of the matrix multiplication job.

4. Each worker thread should write its thread ID to the proc file right before its termination.

5. After completing the matrix multiplication, the main thread has to read the proc file and print the following resulting information on the console (Slide 10 shows an example).

1. Main/parent thread ID

2. Each worker/child thread ID and execution time and context switch times.

6. After completing the matrix multiplication, the program also has to save the result of the matrix multiplication (i.e. the result matrix) to a file named as result.txt.

7. You should hand in a report. In the report,

• You have to explain how you dispatch works to the worker threads.

• For example : by row dispatch or by element dispatch

• You are given four test cases. For each test case, you have to plot the matrix multiplication execution time with the following worker thread numbers.

• Worker thread number: 1,2,3,4,8,16,24,32

• You have to summarize the four charts you plot.

• For example :

1. What happen if the number of threads is less than the number of cores. Why ?

2. What happen if the number of threads is greater than the number of cores. Why ?

3. Anything else you observe

8. The executable and parameters of your multithread program:

./MT_matrix [number of worker threads] [file name of input matrix1] [file name of input matrix2] 9. The VM memory should be set to 4 GB, and the VM cores should be set to 4 cores.

• Steps to set your VM memory and cores are shown in Slide 16.

• If you can’t set your VM memory and cores as requested, you should set them as large as possible.

Race condition

• A race condition is an undesirable situation that occurs when two or more threads can access shared resources and they try to change it at the same time.

• Assume that two threads each increment the value of a global integer variable named count by 1.

• In ideal case , we hope the value of count variable is 2.

• Each thread has its own registers. • Split increment the value by 1 into three steps.

Thread A

1. LW RegA , count

Thread B

1. LW RegB , count

2. ADD RegB , RegB , 1

Critical section

• Parts of the multithreaded program where the shared resource is accessed by more than one thread need to be protected.

• This protected section cannot be entered by more than one thread at a time.

• You can use pthread_mutex_lock(pthread_mutex_t *mutex) and pthread_mutex_unlock(pthread_mutex_t *mutex) to protect critical section.

• In the requirement of multi-threaded program, the fourth requirement mentioned that each

worker thread should write its thread ID to the proc file right before its termination.

the proc file at the same time.

• You can use mutex lock to guard write operation to ensure kernel module can correctly record the required information.

Input/Output Matrix Format

• You are given four test cases. Each test case contains two input matrix files.

• In a matrix file, the first line indicates the row and column of the matrix.

• 1 &lt;= element value &lt;= 1000

• The output matrix format is the same as input matrix format.

An Example Display Format of the Output

• Output format : PID : [PID number]

[ ] ThreadID : [TID number] time : [utime](ms) context switch times : [Context switches]

• Context switches = nvcsw + nivcsw.

• The resolution of time is millisecond.

An Example Format of Charts in the Report

• Chart format:

• Chart title : Elapsed time with different number of worker threads

• X-axis title : number of worker threads

• Y-axis title : Elapsed time (s)

T1 pthread_create()

Elapsed time matrix_multiplication

＝

T2 – T1 pthread_join()

T2

• The resolution of elapsed time is second.

Precautions

Ø You should implement hw2 with C language. You will get files from hw2 github classroom.

Ø You can modify makefile as you want.

Ø Make sure your makefile can compile your codes and create the executable file.

Ø The executable file name should be : MT_matrix.

Ø The kernel module name should be : My_proc.

Ø Make sure your codes can be compiled and run in the DEMO environment introduced in the HW0 slide.

GitHub classroom

Ø Github classroom :

Click here to start your assignment.

Ø Test Cases :

Click here to download test cases.

Grading

Ø If you cannot explain smoothly, you will not get scored.

Reference

1. Matrix multiplication

2. pthreads(7) – Linux manual page

3. Task_struct

4. The Linux Kernel Module Programming Guide

5. The /proc Filesystem

How to set VM memory sizes and core numbers
