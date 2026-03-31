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

### Entry 1 - March 28, 2026, 8:30 PM
**What I did**: Worked on Feature 1 (process priority and ready queue display)

**Details**: 
- Implemented process priority inside the Process class
- Updated the scheduler to display the ready queue
- Tested the output to make sure processes are shown correctly

**Challenges**: Understanding how to integrate priority with the existing scheduling logic

**Solution**: Carefully followed the existing code structure and tested step by step

**Time spent**: 1 hour

---

### Entry 2 - March 28, 2026, 11:30 PM
**What I did**: Worked on Feature 2 (context switch counter)

**Details**: 
- Added a counter to track context switches
- Updated the scheduler to increment the counter after each switch
- Printed the total context switches at the end

**Challenges**: Making sure the counter increments at the correct moment

**Solution**: Placed the counter update after each process execution

**Time spent**: 1 hour

---

### Entry 3 - March 29, 2026, 9:30 PM
**What I did**: Reviewed assignment questions and prepared answers

**Details**: 
- Read all assignment questions carefully
- Analyzed program output to understand behavior
- Started drafting answers based on code and output

**Challenges**: Connecting theoretical concepts with actual program behavior

**Solution**: Compared output with code step by step to understand flow

**Time spent**: 1 hour

---

### Entry 4 - March 30, 2026, 11:40 PM
**What I did**: Implemented Feature 3 (waiting time tracking)

**Details**: 
- Added waitingTime variable to Process class
- Calculated waiting time using System.currentTimeMillis()
- Displayed waiting time summary at the end of execution

**Challenges**: Understanding how to correctly measure waiting time

**Solution**: Tracked process creation time and calculated the difference after execution

**Time spent**: 1.5 hours

---

### Entry 5 - March 31, 2026, 1:30 AM
**What I did**: Completed answers and reflection files

**Details**: 
- Finalized ANSWERS.md and REFLECTION.md
- Verified answers match program output
- Reviewed all work before submission

**Challenges**: Ensuring answers reflect actual implementation

**Solution**: Double-checked answers against code and output

**Time spent**: 1.5 hour

---

### Entry 6 - March 31, 2026, 2:30 AM
**What I did**: Final testing and verification of program output

**Details**:
- Ran the program multiple times to verify consistency
- Checked waiting time and context switch results
- Reviewed output formatting to ensure clarity


**Challenges**: Making sure all features work together correctly without errors


**Solution**: Tested the program step by step and verified results with expected behavior

**Time spent**: 30 minutes
---

## Summary

**Total time spent on assignment**: ~5-6 hours

**Most challenging part**: Implementing waiting time in Feature 3 

**Most interesting learning**: Understanding Round-Robin scheduling and fairness 

**What I would do differently next time**: Start earlier and test each feature immediately after implementing it
