# Lab Report 2, Week 4

<br>

## Code change one

<br>

![Image](lab-report-2-media\codeChanegeOne.png)

<br>
 
[Failure inducing input](https://github.com/hashreds/markdown-parser/blob/main/empty-test-file.md)

<br>

Symptom of failure-inducing output

![Image](lab-report-2-media\changeOneOutput.png)

The original code did not account for a markdown file that does not have any links in it. Because the java doesn't read any links inside the markdown file, it throws a StringIndexOutOfBoundsException, which is the symptom of the bug.

<br>

## Code change two

<br>

![Image](lab-report-2-media\codeChangeTwo.png)

<br>
 
[Failure inducing input](https://github.com/hashreds/markdown-parser/blob/main/image.md)

<br>

Symptom of failure-inducing output

![Image](lab-report-2-media\changeTwoOutput.png)

The original code did not account for a markdown file that has an image instead of a link. The markdown syntax for images and links is very similar, so the java would return a file pathway to the image because it thinks that it is a link, creating a symptom of the bug.

<br>

## Code change three

<br>

![Image](lab-report-2-media\codeChangeThree.png)

<br>
 
[Failure inducing input](https://github.com/hashreds/markdown-parser/blob/main/myExamples.md)

<br>

Symptom of failure-inducing output

![Image](lab-report-2-media\changeThreeOutput.png)

The original code did not account for a markdown file that has unexpected characters inside the link address, such as an extra set parantheses. MarkdownParse would read the first closed parantheses as the end of the link and return the link with missing characters, which is the symptom of the bug.