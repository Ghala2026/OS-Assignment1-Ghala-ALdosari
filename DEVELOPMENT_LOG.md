# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

 **Details**:
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [Mar28, 2026, 12:00 PM]
**What I did**: Set up the GitHub repo and project

**Details**:
 • Created a GitHub account using my university email
 • Forked the starter repository
 • Changed the repository name correctly
 • Added my student ID 
 • Ran the project successfully


**Challenges**:  I was confused about the difference between fork and clone

**Solution**: I watched a short video and understood the difference

**Time spent**: Time spent: 3 hours

---

### Entry 2 -  [Mar28, 2026, 3:00 PM]
**What I did**:  Reviewed the starter code and learned the scheduling logic

**Details**:
 • Studied the Process class and SchedulerSimulation
 • Learned how Round-Robin scheduling works
 • Saw how threads are created and executed
 • Followed the output step by step


**Challenges**:  It was hard to understand how threads work with the queue

**Solution**: I read the code again and connected it with what I learned in OS

**Time spent**:  1 hour

---

### Entry 3 - [Mar29, 2026, 10:05 AM]
**What I did**: Added Feature 1 (Process Priority)

**Details**: 
 • Created a priority field (1–5)
 • Generated random priority values
 • Showed priority in the ready queue

**Challenges**:  I didn’t know where to put the priority generation

**Solution**: I added it inside the constructor

**Time spent**: 30minutes
 
 
---

### Entry 4 -  [Mar29, 2026, 10:36 AM]
**What I did**: Added Feature 2 (Context Switch Counter)

**Details**:
 • Created a static counter
 • Increased it inside the scheduler loop
 • Printed the final count at the end

**Challenges**:  Choosing the correct place to increase the counter

**Solution**: I placed it after taking a thread from the queue

**Time spent**:  1 hour
  

---

### Entry 5 -  [Mar29, 2026, 11:36 AM]
**What I did**: Added Feature 3 (Waiting Time)

**Details**: 
 • Added creation time and waiting time
 • Calculated waiting time using System.currentTimeMillis()
 • Printed the results at the end

**Challenges**:  Understanding how to calculate waiting time

**Solution**:  I made the formula simpler based on execution delay

**Time spent**: 1 hour


---

## Summary

**Total time spent on assignment**: [2 days]

**Most challenging part**:  Calculating waiting time and understanding how threads work

**Most interesting learning**: Learning how Round-Robin scheduling keeps the system fair

**What I would do differently next time**: Start planning earlier and test each feature more carefully
