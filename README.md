# cmsc312-assignment-1--ipc-mechanisms-solved
**TO GET THIS SOLUTION VISIT:** [CMSC312 Assignment 1- IPC Mechanisms Solved](https://www.ankitcodinghub.com/product/cmsc312-assignment-1-ipc-mechanisms-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;118917&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CMSC312 Assignment 1- IPC Mechanisms Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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
<strong>Question 1: Shared Memory&nbsp;</strong>

Write a simple program (example code available on Canvas; can be used as starting point) where <em>processes synchronize via polling</em>. Consider THREE processes: A, B and C. Process A is the master process and will print out the strings from <em>shared memory</em> written by two other writing processes (B first and then C second). Process A needs to ‘wait’ by polling until B and C finish writing their strings to memory. Each of processes A, B and C should be in different code files. Create THREE different shared memory locations: (i) one for storing the pid, (ii) for storing the process identifier (A, B or C) and (iii) for storing the string. Here is the sequence of events that needs to be implemented:

<ol>
<li>Process A writes “&lt;pid&gt;” to the first shared memory location and “A” to the second location. It also writes the string “I am Process A” into the string shared memory location. It then prints out the shared memory location in the following format: “I am Process A – &lt;pid&gt;”. Process A then waits until B and C completes.</li>
<li>Process B first checks if the second shared memory location has a “A” in it. When true, it writes its &lt;pid&gt; into the first shared memory location and the string “I am Process B” into the third shared memory location and then signals A &amp; C that it is complete by writing “B” into the second shared memory location (note: B must wait to write into the process identifier shared memory location until after process A writes “A” there). Then process B quits. At this point, process-A prints out the shared memory location in the following format: “I am Process B – &lt;pid&gt;”.</li>
<li>Process C writes the string “I am Process C” into the string shared memory and its pid into the first shared memory location. It then signals A that it is complete by writing “C” into the second shared memory location (note: C must wait until process B</li>
</ol>
writes “B” into the process identifier shared memory). Then process C

quits. At this point, process-A prints out the shared memory location in the following format: “I am Process C – &lt;pid&gt;”.

<ol start="4">
<li>Process A needs to keep polling the process identifier shared memory location continuously. After process B writes “I am Process B”, process A should be able to print it out. Similarly, after process C writes “I am Process C”, process A needs to be able to print it out. Here some ad-hoc synchronization is needed. Specifically, consider using the usleep() function to delay processes B and C between writing the pid, string and the process identifier to give process A a chance to poll and print. Adjust the delay such that prints happen properly.</li>
<li>Process A is the last one to quit and prints out a “GoodBye &lt;pid&gt;” message at the very end before quitting.</li>
</ol>
<strong>Deliverable: THREE different code files; one each for Process A, B and C. </strong>

<strong>&nbsp;</strong>

<strong>Question 2: Shared Memory&nbsp;</strong>

Create processes A, B and C from the <strong>same</strong> code file using fork. In this case you will have a single code file where the parent process can serve as ProcessA, and two child processes serve as Process B and C.

Consider TWO implementations here: (i) Process B and C are two separate child processes (using two different forks from the parent process); (ii) Process B and C are nested forks (here Process C is forked from within process B and NOT from the parent process).

<strong>Deliverable: TWO different code files; one with regular forks, other one with nested forks.</strong>

<strong>&nbsp;</strong>

<strong>Question 3: Message Queues (9 pts)&nbsp; </strong>

Review the programs (spock.c and kirk.c). Answer (or discuss) questions listed below:

<ol>
<li>Discuss and evaluate what happens when you’re running both in separate windows and you kill one or the other.&nbsp;&nbsp;&nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (3)</li>
<li>Discuss what happens (and why) when you run two copies of kirk. (3)</li>
<li>Discuss what happens (and why) when your run two copies of spock. (3)</li>
</ol>
<strong>Deliverable: A pdf document with the answers to (a), (b) and (c).</strong>

<strong>&nbsp;</strong>

<strong>&nbsp;</strong>

<strong>Question 4: Sort numbers using message queues (15 pts)&nbsp; </strong>

Modify the kirk.c and spock.c programs as follows:

<ul>
<li>c should send a sequence of numbers to spock.c. spock.c then sorts these numbers in ascending order and prints them out.</li>
<li>c should still run in an infinite loop to receive inputs from multiple instances of kirk.c running separately.</li>
<li>Discuss the case when multiple kirk.c execute simultaneously versus</li>
</ul>
each kirk.c instance starts only after the previous one has completed.

<strong>Deliverable: Updated kirk.c and spock.c code files and a pdf document discussing your observations in (iii). </strong>

<strong>&nbsp; </strong>

<strong>Socket programs&nbsp; </strong>

<strong>Question 5: Sort numbers using socket programming (15 pts)&nbsp; </strong>

Modify the client1.cpp and server1.cpp codes to implement a client-server socket program that can sort numbers as explained in Q4.

Note: Multiple clients should be able to send their sequence of numbers to the server simultaneously. The server must “fork” child processes to handle each client separately. Check this link for example code and more explanation:

<a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">https://www.geeksforgeeks.org/design</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">–</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">a</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">–</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">concurrent</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">–</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">server</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">–</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">for</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">–</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">handling</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">multiple</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">–</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">clients</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">–</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">using</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">–</a><a href="https://www.geeksforgeeks.org/design-a-concurrent-server-for-handling-multiple-clients-using-fork/">fork/</a>

<strong>&nbsp;</strong>

<strong>Submission: </strong>

Upload the relevant files on Canvas.

&nbsp;
