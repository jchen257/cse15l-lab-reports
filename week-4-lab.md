# Week 4 Lab Report
## **When Tests Accumulate**
---
## First Code Change
* Code Change
![First Code Change](https://user-images.githubusercontent.com/97651048/151449373-cd36559e-952d-4a94-b783-fef215624696.PNG)
* [Link to Failed Test File](https://github.com/jchen257/markdown-parse/blob/main/markdown1.md)
* Picture Of Test File
* ![Capture1](https://user-images.githubusercontent.com/97651048/151448456-f55dc2ec-22a9-42e7-ae17-f20a64521e84.PNG)
* Symptom of Failure-Inducing Input
![Capture2](https://user-images.githubusercontent.com/97651048/151448677-9e76df3f-ac8b-4121-a31b-8a2085f1cdec.PNG)
* When running the tester file, the markdown file had an open bracket at the very beginning of the file, which was the failure-inducing input. When looking at line 23 of the code change, the code first had an if statement to check for any images in the markdown file. Because this if statement did not account for a bracket as the first character of the markdown file, it produced a bug that resulted in the symptom of the tester throwing an Out of Bounds exception. To fix this, adding a statement to check if there is an open bracket at the beginning of the file solved this bug.
---

## Second Code Change
* Code Change
![Second Code Change](https://user-images.githubusercontent.com/97651048/151484986-c261fa6b-54cf-4140-b75d-414f4bdc3c1e.PNG)
* [Link to Failed Test File](https://github.com/jchen257/markdown-parse/blob/main/markdown3.md)
* Picture Of Test File
* ![Second Bug](https://user-images.githubusercontent.com/97651048/151484852-0c834ac0-6933-4d3d-9eb3-183583492cf9.PNG)
* Symptom of Failure-Inducing Input
![output second](https://user-images.githubusercontent.com/97651048/151485131-4be48ba3-d188-4ec8-846a-95d5effca1b4.PNG)
* When testing the third markdown file, the file had some text that was not a link, such as [bye world], [what], [hello], along with text in the markdown file which was the failure-inducing input. Due to the if statement that checked for brackets or parentheses being below the if statement that checked for images, this produced a bug that produced the symptom of the terminal outputting an Out of Bounds exception. This was solved by moving the if statement that checks for brackets and parentheses above the if statement which checks for images so there is no exception produced. 

---

## Third Code Change
* Code Change
![Third Code Change](https://user-images.githubusercontent.com/97651048/151488736-f5faae6e-455a-4f1a-83d5-1c50ef7cd6ba.PNG)
* [Link to Failed Test File](https://github.com/jchen257/markdown-parse/blob/main/markdown4.md)
* Picture Of Test File
* ![Third Bug](https://user-images.githubusercontent.com/97651048/151489195-8a91163b-bcd1-4548-abd2-6d9bfb704cea.PNG)
* Symptom of Failure-Inducing Input
![output third](https://user-images.githubusercontent.com/97651048/151490517-1d546f7d-03ce-4f89-a910-113bf99f3845.PNG)
* When testing the fourth markdown file, the first line of the file contained an image and text that followed in the next lines. The line containing the image was the failure-inducing input due to the else statement's position which was the bug. The else statement was between the if statements so the if statement to avoid images was not executed before the else statement which resulted in the test failing and thinking the image is a link. This bug was fixed by moving the else statement after both if statements.  



