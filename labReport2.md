# Lab Report 2

## Three Code Changes

1. Code Change 1

![Change 1:](https://github.com/jemilparikh/Cse15L-LabReports/blob/4eaf6d524b294389951beeb8b6696babe49b5bf3/Screen%20Shot%202022-04-24%20at%2011.08.51%20PM.png)

![Failure-Inducing Input in Test File:](https://github.com/jemilparikh/Cse15L-LabReports/blob/af367c34af54f301f0b8943ec0bd43e0fd55d775/Screen%20Shot%202022-04-24%20at%2011.29.27%20PM.png)

![Symptom:](https://github.com/jemilparikh/Cse15L-LabReports/blob/f58c374f0b2c92523b61d5a7f2c13cb22227db89/Screen%20Shot%202022-04-24%20at%2011.52.40%20PM.png)

Since there was text after the closing parenthesis, and there was no conditon that anticipated text after the ')' and the result or symptom was an infinite loop.

2. Code Change 2

![Change 2:](https://github.com/jemilparikh/Cse15L-LabReports/blob/ae674e31eb28ceee9153a34e32d76886dfe5f357/Screen%20Shot%202022-04-25%20at%201.59.26%20AM.png)

![Failure-Inducing Input in Test File:](https://github.com/jemilparikh/Cse15L-LabReports/blob/3669717300f57892c1366de3b516ceda11f3c587/Screen%20Shot%202022-04-25%20at%201.56.43%20AM.png)

![Symptom:](https://github.com/jemilparikh/Cse15L-LabReports/blob/511894c1360f05506781654ba3695d8b922edfe7/Screen%20Shot%202022-04-25%20at%202.05.03%20AM.png)

The symptom was an infinite loop, which was caused by the bug that due to the [] brackets after the link at the end of the test-file2.md, which ensures openBracket is not -1 but closeParen remains -1 which causes currentIndex to keep decreasing and thus the loop keeps going on as currentIndex remains less than markdown.length. The correction was to break from the loop even if any one of openBracket, closeBracket, openParen or closeParen is -1.

3. Code Change 3

![Change 3:](https://github.com/jemilparikh/Cse15L-LabReports/blob/4eaf6d524b294389951beeb8b6696babe49b5bf3/Screen%20Shot%202022-04-24%20at%2011.08.51%20PM.png)

![Failure-Inducing Input in Test File:](https://github.com/jemilparikh/Cse15L-LabReports/blob/af367c34af54f301f0b8943ec0bd43e0fd55d775/Screen%20Shot%202022-04-24%20at%2011.29.27%20PM.png)

![Symptom:](https://github.com/jemilparikh/Cse15L-LabReports/blob/f58c374f0b2c92523b61d5a7f2c13cb22227db89/Screen%20Shot%202022-04-24%20at%2011.52.40%20PM.png)

Since there was text after the closing parenthesis, and there was no conditon that anticipated text after the ')' and the result or symptom was an infinite loop.





