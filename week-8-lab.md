# Week 8 Lab Report
## **What Each Test Should Produce**
* Snippet 1: [`google.com, google.com, ucsd.edu]
* Snippet 2: [a.com, a.com(()), example.com]
* Snippet 3: [https://ucsd-cse15l-w22.github.io/]
## **Implementation of Code Snippets in MarkdownParseTest.java**
![Capture](https://user-images.githubusercontent.com/97651048/155811758-200897a2-5738-4ff9-aba8-1d496ebd9f43.PNG)
## **Output Of My Implementation for Snippet Tests**
![Capture1](https://user-images.githubusercontent.com/97651048/155812952-285302bb-9fcb-407a-8014-952afc6947ed.PNG)
* Snippet 1: **Failed** ``expected:<[`google.com, google.com, ucsd.edu]> but was:<[url.com, `google.com, google.com, ucsd.edu]>``
* Snippet 2: **Failed** `expected:<[a.com, a.com(()), example.com]> but was:<[a.com, a.com((, example.com]>`
* Snippet 3: **Failed** expected:<[https://ucsd-cse15l-w22.github.io/]> but was:<[
    https://www.twitter.com
,
    https://ucsd-cse15l-w22.github.io/
, github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



]>
## **Output Of Reviewed Implementation for Snippet Tests**
![Capture2](https://user-images.githubusercontent.com/97651048/155814741-89ac063c-d420-4755-ab9c-06eff32201ad.PNG)
* Snippet 1: **Failed** ``<[`google.com, google.com, ucsd.edu]> but was:<[url.com, `google.com, google.com]>``
* Snippet 2: **Failed** `expected:<[a.com, a.com(()), example.com]> but was:<[a.com, a.com((]>`
* Snippet 3: **Failed** expected:<[https://ucsd-cse15l-w22.github.io/]> but was:<[
    https://www.twitter.com
, 
    https://ucsd-cse15l-w22.github.io/
, github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



]>
* For Snippet 1, I think there is a small code change that will fix cases that use inline code with backticks. Since my program thought the code with backticks was a link when it is not, I would create an if statement to check whether or not there is a backtick outside the brackets. If the backtick is inside the brackets, then it would still be a link since the VScode preview registered it as a link so I would only have to consider backticks outside of the brackets
*  For Snippet 2, I also think there is a small code change that will allow me to fix cases of parentheses, brackets, and escaped brackets. Since my program recognized two out of the three links correctly, the only case I would need to consider is a nested parenthesized url. In order to account for these cases, I would create an if statement that will check if there are more closing parentheses next to each other and would set closeParen to the last closing parentheses.
*  For Snippet 3, I think there is a small code change that will fix cases of newlines in brackets and parentheses for my program. In this code change, I need to consider cases with line breaks in the bracket since those do not count as links and also cases where the parentheses have line breaks which are considered links. I would create an if statement checking if there are any line breaks between either the brackets or the parentheses to get the correct output.


