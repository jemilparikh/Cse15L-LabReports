# Lab Report 4

## Links

* [Link to my markdown-parse repository](https://github.com/Mashyuf/markdown-parser)
* [Link to the repostiory I reviewed in Week 7](https://github.com/cmy0357/markdown-parser)

## Snippet 1:

* Expected Output in CommonMark:

![Expected Output in CommonMark:](https://jemilparikh.github.io/Cse15L-LabReports/snippet1expectedOutput.png)

* Turning it into a test:

![Turning it into a test:](https://jemilparikh.github.io/Cse15L-LabReports/Snippet%201%20Test.png)

* Output after running test (failed) for my implementation:

![Output after running test (failed) for my implementation:](https://jemilparikh.github.io/Cse15L-LabReports/Failure%20Snippet1%20Test.png)

* Output after running test (failed) for reviewed implementation:

![Output after running test (failed) for reviewed implementation:](https://jemilparikh.github.io/Cse15L-LabReports/Snippet%201%20Test%20Failed%20Reviewed.png)

## Snippet 2:

* Expected Output in CommonMark:

![Expected Output in CommonMark:](https://jemilparikh.github.io/Cse15L-LabReports/snippet2expectedOutput.png)

* Turning it into a test:

![Turning it into a test:](https://jemilparikh.github.io/Cse15L-LabReports/Snippet%202%20Test.png)

* Output after running test (failed) for my implementation:

![Output after running test (failed) for my implementation:](https://jemilparikh.github.io/Cse15L-LabReports/Failure%20Snippet2%20Test.png)

* Output after running test passed for reviewed implementation.

## Snippet 3:

* Expected Output in CommonMark:

![Expected Output in CommonMark:](https://jemilparikh.github.io/Cse15L-LabReports/snippet3expectedOutput.png)

* Turning it into a test:

![Turning it into a test:](https://jemilparikh.github.io/Cse15L-LabReports/Snippet%203%20Test.png)

* Output after running test (failed) for my implementation:

![Output after running test (failed) for my implementation:](https://jemilparikh.github.io/Cse15L-LabReports/Failure%20Snippet3%20Test.png)

* Output after running test (failed) for reviewed implementation:

![Output after running test (failed) for reviewed implementation:](https://jemilparikh.github.io/Cse15L-LabReports/Snippet%203%20Test%20Failed%20Reviewed.png)


## Answers

1. Answer 1: It is indeed possible to allow for backticks with inline code in my program with a minor change. In the if condition that searches for the openBracket, openParen, closeParen and closeBracket, one can search for any backtick if it exists within that entire text (from openBracket to closeBracket, or before openBracket). If it does, the entire text shouldn't be considered as a link and can be skipped (currentIndex would be closeBracket + 1). If not, go ahead as usual by returning the link between openParen and closeParen.

2. Answer 2: While it is possible to account for the nested parentheses, brackets and escaped brackets, it is a tedious task as one would have to go through the entire string through a long loop to know if the link is in the proper format alongwith the accurately nested brackets and parenthesis. Hence, it is not a small change.

3. Answer 3: Yes, it is relatively easy to implement the code to account for spaces in brackets and parentheses. Again there can be a condition which checks for any " " (empty space) or "\n" (new lines) in between openParen and closeParen. If there, change currentIndex to closeBracket + 1. If not, go ahead with returning the link between openParen and closeParen.

## Tests that passed

In the reviewed repository, the test for snippet 2 passed. This is because the expected condition in the test was similar to the outcome because the MarkdownParse code in this reviewed repository doesn't account for nested parenthesis and excludes any text after the first closeParen (as with '(a.com(()))'). This was specifically assumed in the test as the expected outcome and hence it passed. However the code in markdownParse is still not correct for all cases that nest brackets, parentheses or escaped brackets.


