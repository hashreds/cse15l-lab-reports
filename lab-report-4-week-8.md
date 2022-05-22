# Lab Report 4, Week 8

<br>

[Link to my repo](https://github.com/hashreds/markdown-parser)

[Link to repo we reviewed](https://github.com/zayverrulez/markdown-parser)

<br>

## Code snippets test (Snippet 1) on my repo and other repo

<br>

Based on the preview below, we expect "`google.com", "google.com", "ucsd.edu"

![Image](lab-report-4-media\codeSnippetsExpected.png)

Code for test on both mine and other repo:

![Image](lab-report-4-media\codeSnippetsTest.png)

My implementation fails the test:

![Image](lab-report-4-media\codeSnippetsTestMineFailingAgain.png)

Their implementation also fails the test:

![Image](lab-report-4-media\codeSnippetsTheirTestFailing.png)

<br>

## Wacky brackets test (Snippet 2) on my repo and other repo

<br>

Based on the preview below, we expect "a.com", "a.com(())", "example.com"

![Image](lab-report-4-media\wackyBracketsExpected.png)

Code for test on both mine and other repo:

![Image](lab-report-4-media\wackyBracketsCode.png)

My implementation fails the test:

![Image](lab-report-4-media\wackyBracketsMineFailsAgain.png)

Their implementation also fails the test:

![Image](lab-report-4-media\wackyBracketsOtherFailing.png)

<br>

## Long titles test (Snippet 3) on my repo and other repo

<br>

Based on the preview below, we expect "https://www.twitter.com", "https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule", "https://cse.ucsd.edu/"

![Image](lab-report-4-media\longTitleExpected.png)

Code for test on both mine and other repo:

![Image](lab-report-4-media\longTitlesCode.png)

My implementation fails the test.

![Image](lab-report-4-media\longTitleMineFails.png)

Their implementation also fails the test:

![Image](lab-report-4-media\longTitlesOtherFails.png)

<br>

## Questions

1. I think a small code change I could make to get my implementation to work with backticks is to add a condition when parsing the markdown file that would ignore any backticks. Backticks are not a valid input in the syntax for links, so the parser should leave them out of the link.

2. A code change to make my markdown parser pass the test for the second snippet would be more involved and longer than ten lines. We would have to implement some kind of helper method that will ignore sets of brackets that don't have parentheses next to them and incorporate links that have parentheses next to the brackets.

3. A code change I could make to this test that would not be a short one would be to add a helper method that checks all lines to find the closing parentheses. The parser only looks on the same line for the closed bracket, but it should be checking all of the lines until the end of the file.

