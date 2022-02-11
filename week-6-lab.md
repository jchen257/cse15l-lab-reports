# Week 6 Lab Report
## **Streamline SSH Configuration**
---
## Editing `.ssh/config` File 
---
* Since logging in to `ieng6` typically requires typing out your course account (cs15lwi22zzz@ieng6.ucsd.edu) which is hard to remember, you can streamline this process by creating a nickname for this account
* Open `.ssh/config` in VSCode
* ![Capture](https://user-images.githubusercontent.com/97651048/153681607-478b5083-6825-47f1-80c1-b2573b3792a2.PNG)
* Change the host name to your desired nickname and save the changes
* This nickname will be the phrase you will type to use commands like `ssh` or `scp`

## Using Nickname With Commands `ssh` and `scp`
---
![Capture1](https://user-images.githubusercontent.com/97651048/153681691-51361d83-2d90-428f-94e5-5f83a913886b.PNG)
* After changing the host name, you can now use this nickname to ssh into your account without having to use the course account
![Capture2](https://user-images.githubusercontent.com/97651048/153681773-118a8a4c-8e1f-4f7a-a694-7d02742da8c6.PNG)
* This makes commands like `ssh` or `scp` easier since you do not need to remember the course account and just need the nickname. Here is an example of `scp` with the nickname
![Capture3](https://user-images.githubusercontent.com/97651048/153681876-6da36262-b62d-46a7-b296-c6f92d305d13.PNG)
* As shown in the example, `scp` worked with the nickname and TestFile.java is now in my remote account
* Using this technique, logging into `ieng6` is now quicker and easier to do now that you do not need to remember your course account




