# Interview Questions Encountered

The following is a list of interview questions I've encountered at some point.

## Most Recent Interviews (as of 02/2021)

Before I start this section, note to self that section titles like "recent interviews" quickly become irrelevant and/or completely incorrect. That being said, over the last 2 months, I've done a handful of interviews and there are a number of (mostly knowledge-based) questions that I didn't know the answers to.

- What are some best practices (that you would teach a junior engineer) when developing for real-time systems?
- In C++ what is the difference between malloc/new and free/delete?
- Given a sorted list, how would you efficiently find a number in the list?
  - after answering with binary search, the follow-up question was is that always the most efficient?
  - I responded that it would be the most efficient without knowing more about the data set, and tried to describe exponential search as an option that could be more efficient (but I wasn't sure when that would be the case)
- What are class Enums in C++?
- When using atomic operations (perhaps specific to the GCC compiler?), what are the 6 memory models you can use? Do you understand the difference between them?

## Recent Interviews

I did 2 non-coding, though still technical interviews recently with hiring managers at 2 different companies. I want to capture the questions in general, but mostly I want to capture the questions that caught me off guard.

- interview 1:
  - what version of C++ did you use most recently?
  - Are you familiar with modern c++ features? lambda functions, others?
  - Are you familiar with QT as a GUI framework?
- interview 2:
  - what is the difference between public, private and protected (I originally described the parent child relationship backwards in regards to protected, though I genuinely think that was just fumbling of words not mixing up the concept)
    - when would you use the protected keyword? give an example
  - given a point x,y how far is the point from 0,0?
    - what is the angle between the vector pointing from 0,0 to x,y and the y-axis? -- I mixed 2 things up here:
      - sin, cos, tan take an angle as the argument (not the result), so instead of sin/cos/tan I wanted to use arcsine/arccosine/arctan
      - I forgot/mixed up the phrase 'SOHCAHTOA', specifically thinking the first H was an A, so instead of answering tan(y/x) I answered sin(y/x)
      - for reference the correct answer was atan(y/x)
    - Why do programming languages have 2 different atan functions (atan and atan2)? -- I didn't know this off the top of my head, but with the hint of "what happens if x and y are both positive, vs x and y both being negative" I remembered/realized the answer was that without separating x and y, the answer could be ambiguous (i.e. both positive results in Q1, while both negative should be Q4, yet without separating x,y they would give the same answer)
  - What is your familiarity with algorithms? gradient descent, simulated annealing, Dijkstra's, A* etc.
    - roughly how does Dijkstra's work? why is it faster than BFS or DFS?

## Older Interviews

### Knowledge-based questions

- Why would you use a virtual destructor in c++?
- What is the decorator design pattern (question was asked referring to Java)
- What is the .profile file for in Linux?
- What is Agile?
- Java collections (set vs list vs map) -> is an array a list?
- Different versions of c++ vs java question -> what is your favorite part of each? least favorite? why?
- How is a thread different from a process?
- What is deadlock? live lock? how are they different?
  - How do you prevent each of them?

### Design questions

- Design typeahead search (search suggestions)
- Design Bitly
- Design Minesweeper
- Design system to distribute binary/executable file to many machines

### Algorithm questions

- Merge k sorted lists ([Leetcode-23](https://leetcode.com/problems/merge-k-sorted-lists/))
