# Lab Report 5

## How did I find tests with different results?

* Answer 
I ran vimdiff with the two different implementations' results.txt files using the following command:

        $ vimdiff my-markdown-parser/results.txt cse15lsp22-markdown-parser/results.txt
        
This results in a line by line comparison of the two results.txt files from two different markdown-parser repositories. The tests that have differences are highlighted. I then manually choose two tests for the purpose of this lab report from the ones highlighted.

## Link to test-files with different results
 
* Test-File 1: [Link](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/490.md)
* Test-File 2: [Link](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/491.md)

## Which implementation is correct?

* For Test-File 1, my implementation is incorrect. 
* For Test-File 2, both the implementations are incorrect.

## Actual Output VS Expected Output

* ![Actual Output:](https://jemilparikh.github.io/Cse15L-LabReports/testFilesActualOutput.png)
Note: Left side of this picture shows the outputs for results.txt of my markdown-parser repository. Right side shows the outputs for results.txt of the provided markdown-parser. Both test-files 490 and 491's outputs shown consecutively in the same picture.

* Expected Output using CommonMark: 

  ![Test-File 490:](https://jemilparikh.github.io/Cse15L-LabReports/Screen%20Shot%202022-06-05%20at%2011.32.47%20PM.png)

  Note: Leads to no link in CommonMark.

  Test-File 491:

  ![Test-File 491:](https://jemilparikh.github.io/Cse15L-LabReports/https://github.com/jemilparikh/Cse15L-LabReports/blob/main/Screen%20Shot%202022-06-      05%20at%2011.33.32%20PM.png)

Note: Leads to the following [link](https://spec.commonmark.org/dingus/b)c).

## Fix

* Test-File 490:

My implementation of markdown-parser is incorrect for this test-file as it does not match the correct output of a simply returning no link and basic '[]'.

 
 
 
        
        


