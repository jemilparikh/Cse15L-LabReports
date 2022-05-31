# Lab Report 4

## Links

* [Link to my markdown-parse repository](https://github.com/Mashyuf/markdown-parser)
* [Link to the repostiory I reviewed in Week 7](https://github.com/cmy0357/markdown-parser)

## Snippet 1:

* Expected Output in CommonMark:

![Expected Output in CommonMark:](https://jemilparikh.github.io/Cse15L-LabReports/snippet1expectedOutput.png)

* Turning it into a test:

![Turning it into a test:](https://jemilparikh.github.io/Cse15L-LabReports/Screen%20Shot%202022-05-31%20at%202.47.56%20PM.png)

* Output after running test (failed) for my implementation:

![Output after running test (failed) for my implementation:](https://jemilparikh.github.io/Cse15L-LabReports/Screen%20Shot%202022-05-31%20at%202.43.26%20PM.png)

* Output after running test (failed) for reviewed implementation:

![Output after running test (failed) for reviewed implementation:](https://jemilparikh.github.io/Cse15L-LabReports/Screen%20Shot%202022-05-31%20at%202.42.56%20PM.png)

## Snippet 2:

* Expected Output in CommonMark:

![Expected Output in CommonMark:](https://jemilparikh.github.io/Cse15L-LabReports/snippet2expectedOutput.png)

* Turning it into a test:

![Turning it into a test:](https://jemilparikh.github.io/Cse15L-LabReports/2.png)

* Output after running test (failed) for my implementation:

![Output after running test (failed) for my implementation:](https://jemilparikh.github.io/Cse15L-LabReports/8.png)

![Output after running test (failed) for reviewed implementation:](https://jemilparikh.github.io/Cse15L-LabReports/5.png)

## Snippet 3:

* Expected Output in CommonMark:

![Expected Output in CommonMark:](https://jemilparikh.github.io/Cse15L-LabReports/snippet3expectedOutput.png)

* Turning it into a test:

![Turning it into a test:](https://jemilparikh.github.io/Cse15L-LabReports/3.png)

* Output after running test (failed) for my implementation:

![Output after running test (failed) for my implementation:](https://jemilparikh.github.io/Cse15L-LabReports/9.png)

* Output after running test (failed) for reviewed implementation:

![Output after running test (failed) for reviewed implementation:](https://jemilparikh.github.io/Cse15L-LabReports/6.png)


## Answers

1. Answer 1: It is indeed possible to allow for backticks with inline code in my program with a minor change. In the if condition that searches for the openBracket, openParen, closeParen and closeBracket, one can search for any backtick if it exists within that entire text (from openBracket to closeBracket, or before openBracket). If it does, the entire text shouldn't be considered as a link and can be skipped (currentIndex would be closeBracket + 1). If not, go ahead as usual by returning the link between openParen and closeParen.

2. Answer 2: While it is possible to account for the nested parentheses, brackets and escaped brackets, it is a tedious task as one would have to go through the entire string through a long loop to know if the link is in the proper format alongwith the accurately nested brackets and parenthesis. Hence, it is not a small change.

3. Answer 3: Yes, it is relatively easy to implement the code to account for spaces in brackets and parentheses. Again there can be a condition which checks for any " " (empty space) or "\n" (new lines) in between openParen and closeParen. If there, change currentIndex to closeBracket + 1. If not, go ahead with returning the link between openParen and closeParen.



