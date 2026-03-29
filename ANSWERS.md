# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**
A process is an independent program in execution with its own memory space and system resources, while a thread is a lightweight unit of execution within a process that shares the same memory and resources. Processes are more expensive to create and manage, whereas threads are faster and more efficient. In this assignment, threads were used instead of processes because they allow easier communication and shared access to the ready queue. Additionally, threads reduce overhead and are more suitable for simulating scheduling algorithms like Round-Robin. This aligns with concepts discussed in Operating System Concepts (Silberschatz et al., 10th Edition).

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**
In Round-Robin scheduling, when a process does not finish within its time quantum, it is preempted and moved to the end of the ready queue. This allows other processes to get CPU time, ensuring fairness among all processes. The process will wait in the queue until it gets another turn.
▶ P1 executing quantum [4000ms]
⏸ P1 completed quantum 4000ms │ Overall progress: [████████████████░░░░] 81%
Remaining time: 916ms
↻ P1 yields CPU for context switch

P1 (Priority: 2) added...

│ [P3 → P4 → P5 → P6 → P7 → P8 → P9 → P10 → P11 → P12 → P1]

In this example, process P1 did not finish execution after its time quantum of 4000ms because it still had 916ms remaining. As a result, the scheduler preempted it and placed it back at the end of the ready queue, as shown in the queue where P1 appears last. This demonstrates how Round-Robin scheduling cycles processes fairly until they complete execution.











[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**
In this simulation, each process behaves like a thread and transitions through different states during execution. Below is the lifecycle of process P1 based on the output:




[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**:
    P1 enters the New state when it is first created:
P1 (Priority: 2) added...

   
2. **Runnable**:
   After being created, P1 is placed in the ready queue and waits for CPU execution:
│ [P2 → P3 → P4 → P5 → P6 → P7 → P8 → P9 → P10 → P11 → P12]
   

3. **Running**: 
P1 becomes Running when it is assigned CPU time:
▶ P1 executing quantum [4000ms]

4. **Waiting**:
Since P1 did not finish, it is preempted and returned to the ready queue:
↻ P1 yields CPU for context switch
P1 (Priority: 2) added...


5. **Terminated**:
Finally, P1 completes execution when its remaining time reaches zero:
▶ P1 executing quantum [916ms]
⏸ P1 completed quantum 916ms │ Overall progress: [████████████████████] 100%
Remaining time: 0ms
✓ P1 finished execution!




---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**  









### Example 1:

**Description**: 
A web server handles multiple user requests simultaneously, where each request is treated as a separate thread.



**Why Round-Robin works well here**: 
time, preventing any single request from monopolizing the server. This improves responsiveness and ensures all users receive timely service.

### Example 2: 
**Description**: 


Modern operating systems manage multiple applications running at the same time, such as browsers, music players, and background services.

**Why Round-Robin works well here**: 

Round-Robin provides fairness by giving each process equal CPU time. It ensures that no application is starved and maintains system responsiveness, especially in interactive environments.



---

## Summary

**Key concepts I understood through these questions:**
1. Difference between threads and processes
 2. Behavior of Round-Robin scheduling
 3. Thread lifecycle states

**Concepts I need to study more:**
1. Advanced synchronization techniques
 2. Deadlocks and race conditions
