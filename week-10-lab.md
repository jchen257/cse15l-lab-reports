# Week 10 Lab Report
---
## **How I Found The Tests**
* I found the tests with different results by using `diff` on both of the results of the bash for loop for implementations of MarkdownParse. After seeing the differences between each of the results, I picked two random tests that looked different from each other which will be the ones I will explain.
---
## **Test One**
**Difference**
``` 
1065c1062
< [] (My Implementation)
---
> [train.jpg] (Implementation Provided For Lab 9)
```
**Markdown File**
```
![foo](train.jpg)
```
**Expected Outcome**
```
[] (From https://spec.commonmark.org/dingus/)
```
**Who's Correct and Describing the Bug**
* In this test which was markdown file 577.md, my implementation of MarkdownParse was correct since it did not recognize the image to be a link while the implementation provided by the lab did recognize it as a link. To correct this bug in the lab-provided implementation, I would address the cases when the markdown file has an image in it. Since images and links look very similar in formatting, this is the reason why the lab implementation thought it was a link. To fix this, I would create an if statement that checks for ! which is what is different from images and links. I would code it similar to how I did it in my implementation

**How to Fix The Bug**
* Add an if statement to check for images
```
            if (nextOpenBracket != 0 && markdown.substring(nextOpenBracket-1, nextOpenBracket).equals("!")){
                currentIndex = closeParen + 1;
                continue;
            }
```

## **Test Two**
**Difference**
``` 
230c230
< [] (My Implementation)
---
> [baz] (Implementation Provided For Lab 9)
```
**Markdown File**
```
[foo]: <bar>(baz)

[foo]
```
**Expected Outcome**
```
[] (From https://spec.commonmark.org/dingus/)
```
**Who's Correct and Describing the Bug**
* In this test which was markdown file 201.md, my implementation of MarkdownParse was correct since it did not recognize anything in the Markdown file to be a link while the lab-provided implementation found a link called `baz`. To fix this bug, I would address cases where the parentheses are not directly after the closing bracket. If the parentheses are not directly after the closing bracket, MarkdownParse should not recognize it as a link so adding a if statement to check for this would help address this bug in the lab-provided implementation.


**How to Fix The Bug**
* I would add another if statement. In this if statement, I would check if the index of the parentheses is right after the index of the closing bracket to see if it is actually a link.

