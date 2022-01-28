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
* When running the tester file, the markdown file had an open bracket at the very beginning of the file, which was the failure-inducing input. When looking at line 23 of the code change, the code first had an if statement to check for any images in the markdown file. Because this if statement did not account for a bracket as the first character of the markdown file, it produced a bug which resulted in the symptom of the tester throwing an Out of Bounds exception. To fix this, adding a statement to check whether there is an open bracket in the beginning of the file solved this bug but other bugs mentioned next still produced a failed test.
---

## Second Code Change
* Code Change
![Second Code Change](https://user-images.githubusercontent.com/97651048/151484986-c261fa6b-54cf-4140-b75d-414f4bdc3c1e.PNG)
* [Link to Failed Test File](https://github.com/jchen257/markdown-parse/blob/main/markdown3.md)
* Picture Of Test File
* ![Second Bug](https://user-images.githubusercontent.com/97651048/151484852-0c834ac0-6933-4d3d-9eb3-183583492cf9.PNG)
* Symptom of Failure-Inducing Input
![output second](https://user-images.githubusercontent.com/97651048/151485131-4be48ba3-d188-4ec8-846a-95d5effca1b4.PNG)
* When testing the third markdown file, the file had some text that was not a link, such as [bye world], [what], [hello], along with text in the markdown file which was the failure-inducing input. Due to the if statement that checked for brackets or parentheses being below the if statment that checked for images, this produced a bug which produced a symptom of the terminal outputting an Out of Bounds exception. This was solved by moving the if statement that checks for brackets and parentheses above the if statement which checks for images so there is no exception produced. 
