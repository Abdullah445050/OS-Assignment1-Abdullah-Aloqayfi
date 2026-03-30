# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

A process is an independent program with its own memory space and system resources, while a thread is a smaller unit of execution that runs inside a process. Threads are lighter than processes because they share memory with other threads in the same program, which makes them faster to create and easier to coordinate. In this assignment, threads were more suitable because the scheduler simulation needs many tasks to be created, started, paused, and re-queued efficiently. The code creates a new `Thread` for each process and manages them through a ready queue, which is simpler and more efficient than creating separate operating system processes. This makes the Round-Robin simulation practical and keeps the scheduling logic focused on CPU sharing rather than process management.


---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

In Round-Robin scheduling, if a process does not finish within its time quantum, it gives up the CPU and returns to the ready queue. This allows other processes to run before the same process gets another turn, which improves fairness. In my output, this happened with P1: it executed for 3000ms, still had 2005ms remaining, yielded the CPU, and was added back to the ready queue. The same pattern also happened with several other processes such as P2, P3, P9, and P11, which shows the scheduler is rotating processes fairly.

Example from my output:
```text
? P1 executing quantum [3000ms]
? Quantum progress: [???????????????] 100%
? P1 completed quantum 3000ms ? Overall progress: [????????????????????] 59%
   Remaining time: 2005ms
? P1 yields CPU for context switch

? P1 added to ready queue ? Priority: 1 ? Burst time: 5005ms
```

**Explanation of example:**
This snippet shows that P1 was allowed to run only for one time quantum, which was 3000ms. Since its total burst time was 5005ms, it still had 2005ms left after the first turn, so it could not finish in one run. The scheduler then re-added P1 to the ready queue so other processes could execute first. This re-queueing behavior is important because it prevents one long process from monopolizing the CPU and gives all processes a fair chance to progress.

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

For P1, the thread begins in the New state when the program creates it with `new Thread(process)` inside the scheduler before it starts execution. It becomes Runnable when thread.start() is called, meaning it is ready to run and waiting for CPU scheduling. It enters the Running state when the scheduler actually gives it CPU time and the run() method starts executing, which is visible in the output when P1 begins its quantum. During execution, the thread can be considered in a Waiting or timed-waiting situation when Thread.sleep() is used to simulate the passage of execution time. Finally, P1 reaches the Terminated state after its remaining time becomes 0, which is shown in the output when P1 finishes its last quantum and the program prints P1 finished execution!

1. **New**: P1 is in the New state when its thread is created but before start() is called

2. **Runnable**: P1 becomes Runnable after thread.start() and waits for its turn in the scheduler.

3. **Running**: P1 is Running when the output shows P1 executing quantum [3000ms] and later P1 executing quantum [2005ms]

4. **Waiting**: P1 enters a waiting or timed-waiting state during the simulated execution period when Thread.sleep() is used inside the code.

5. **Terminated**: P1 is Terminated after its second execution when the output shows Remaining time: 0ms followed by P1 finished execution!

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: Web Server

**Description**: 
A web server often handles many client requests at the same time, and each request can be processed by a separate thread.

**Why Round-Robin works well here**: 
Round-Robin helps ensure that no single request uses the CPU for too long while other requests are waiting. This improves fairness and keeps the server responsive, especially when many users connect at the same time. The idea is similar to this assignment, where each process gets a limited time quantum and then returns to the queue if it still needs more CPU time.

### Example 2: Operating System Task Scheduling

**Description**: 
An operating system may run many interactive programs at once, such as a browser, media player, editor, and background services

**Why Round-Robin works well here**: 
Round-Robin is useful because it gives each task a fair share of CPU time and prevents starvation. It is especially good for interactive systems because users expect all programs to remain responsive instead of one program blocking the others. This is exactly what happened in the simulation, where 20 processes shared the CPU using a fixed 3000ms time quantum and the scheduler recorded 41 context switches before all processes completed

---

## Summary

**Key concepts I understood through these questions:**
1. The difference between a process and a thread, especially in terms of memory sharing and overhead
2. How Round-Robin scheduling re-queues unfinished processes to maintain fairness.
3. How a thread moves through states such as New, Runnable, Running, Waiting, and Terminated during execution

**Concepts I need to study more:**
1.  Thread synchronization and race conditions
2.  More advanced scheduling algorithms and how they compare with Round-Robin
