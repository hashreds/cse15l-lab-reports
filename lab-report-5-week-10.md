# Lab Report 5, Week 10

<br>

### How I found the differing tests

<br>

During lab 9, I ran stored the results of running `bash script.sh` inside a text file for the staff's markdown parser and my own. When I ran my own markdown parser with `basg script.sh`, I ran into numerous infinite loops triggered by the test files. I deleted the `.md` extension from the error-inducing test files, and I have chosen two of these (test-files 12 and 14) to be my chosen files.

<br>

### Links to the error-inducing tests

[Test 12](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/12.md)

[Test 14](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/14.md)

<br>

### For test 12:

My output is incorrect because it shows an infinite loop, while the staff implementatino is correct because it matches the output on the CommonMark demo site.

My markdown parser's output:

![Image](lab-report-5-media\12-failing.png)

Staff's markdown parser output:

![Image](lab-report-5-media\staff-12.png)

Based on the preview below, expect `[]` because there are no valid links in the file.

![Image](lab-report-5-media\12-actual.png)

In the screenshot of my code below, the issue is that the variables that store the indices of the open brackets and the open parentheses do not know how to account for a situation when the parentheses come before the brackets. In the 12th test file, the brackets come before the parentheses, and this throws the indices of the brackets and the currentIndex, which causes the infinite loop.

![Image](lab-report-5-media\12-debug.png)


<br>

### For test 14:

Both my ouput and the staff output is incorrect in this case, since my markdown parser throws an infinite loop and the staff's markdown parser throws a link that is not valid.

My markdown parser's output:

![Image](lab-report-5-media\14-failing.png)

Staff's markdown parser output:

![Image](lab-report-5-media\staff-14.png)

Based on the preview below, expect `[]` because there are no valid links in the file.

![Image](lab-report-5-media\14-actual.png)

In the screenshot of my MarkdownParse.java code below, the issue is similar to what caused the inifnite loop in test file 12. In test file 14, there is a link with the correctly-ordered []() format, but then there is a set of square brackets without a set of parentheses that follow the square brackets. Thus, the intOpen paren variable is never assigned to a value and currentIndex is never updated, so the while () condition is always true and it runs an infinite amount of times.

![Image](lab-report-5-media\14-debug.png)