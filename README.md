# Summary of Learning

## Problems chosen

- Problem 16
- Problem 19
- Problem 22
- Problem 23
- Problem 24

## Which problem(s) gave you the most trouble? Did you avoid any problem that is too challenging to finish by deadline? Did you ask questions to AI/instructor?

I think #16, where every odd position is 1, was the trickiest, even though the NFA only has 2 states. I initially made only `q0` the accepting state, since it was my even state. After tracing some example inputs `101` and `1` by hand, which ended on `q1` and were rejected although they satisfy the language, I realized that accepting a string depends on which state I am in when the input ends. Since the string can legally end right after an odd-position 1 (`q1`) or after an even-position symbol (`q0`), both states needed to be accepting.

I did not skip any of the 5 problems I chose. I spent time building and batch-testing all NFA designs carefully in JFLAP with test inputs. I also
verified my work with Claude to get explanation on where I did not understand.

## Which problem(s) surprised you with a "gold-st-ring"? Which next state(s) did you not account for in the subset of next states? why? How to make sure you avoid such errors in your future flight/traffic/compiler state controller tasks, or in the near future, the course projects/exams?

- Question 16: `q1` was missing an accepting state because I did not account for the state right after the string input satisfied the odd-position constraint initially.

- Question 19: I resued `q1` for both the second state and final accepting state, making the diagram ambiguous even though the drawn transitions were correct. I renamed the accepting state to `q3`

- Question 22-24: I did not account for the self-loops on 0, making the diagram reject any valid strings with one or more zeros in them.

In the future, I will try to avoid this by asking myself two questions:

- For every symbol in the alphabet, does this state have transition arrow for it, and if not, is that for any reason?
- Is this state a valid end point for the string?

## Other insights/comments/questions that you want the grader/instructor to know

- Working through each design by hand-tracing test string for every chosen problem on paper before building in FJLAP
- All chosen problems have full step-by-step traces in JFLAP, exceeding the minimum of 3
