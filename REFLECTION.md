# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**

In this assignment, I learned that multithreading allows multiple tasks to run at the same time within a single program. Each process was executed as a thread in the Round-Robin scheduler.. Compared to processes, threads communicate more quickly since they share the same memory. I also observed thread states like Runnable and Running while executing the processes in the simulation. Thread.sleep() was used to mimic actual execution time. Implementing Round-Robin scheduling in the code helped me understand how threads share CPU time. I also came to understand how crucial it is to handle threads carefully in order to prevent problems. In general, this assignment improved my comprehension of practical threading ideas.

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**

Understanding how Round-Robin scheduling operates with threads was the most difficult aspect of this project. It was difficult to track how processes move between execution and the ready queue during the simulation. Implementing Feature 3 (waiting time) required careful handling of timing using System.currentTimeMillis(). At first, I didn't understand how waiting time should be computed. Because execution is not always linear, debugging thread behavior was especially challenging. It was also difficult to manage several features without altering the current code. Nonetheless, this enhanced my debugging abilities.

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**

I overcame the challenges by breaking the problem into smaller parts. Before adding new features, I made sure I understood the original code. After that, I tested each feature independently to make sure it functioned properly. In order to prevent errors, I very carefully went over the assignment instructions. I was able to find logical problems by debugging step-by-step. I used print statements to track how threads were executing step by step. Lastly, I confirmed that my output exhibited the anticipated behavior.

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**

Multithreading is used in many real-world applications such as web browsers and mobile apps. For instance, a browser can use threads to load several tabs simultaneously. Threads are used in mobile apps to carry out background operations without causing the user interface to freeze. Additionally, game engines use threads to manage input, graphics, and physics all at once. To effectively manage numerous client requests, servers employ threads. This assignment helped me understand how these systems work internally. Additionally, it demonstrated the significance of scheduling for performance.

---

## Additional Reflections (Optional)

### What would you like to learn more about?

I would like to learn more about thread synchronization and how to avoid race conditions. I am also interested in learning about deadlocks and how they can be prevented. Additionally, I want to understand advanced scheduling algorithms beyond Round-Robin.

---

### How confident do you feel about multithreading concepts now?

Intermediate. I understand the basics of multithreading and scheduling, but I still need more practice with complex scenarios and synchronization.

---

### Feedback on the assignment

The assignment was very useful for understanding practical threading concepts. It was challenging but helped improve problem-solving skills. The step-by-step structure made it easier to follow.
