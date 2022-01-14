# Week 2 Lab Report
## **Remote Access**
---

## Installing VSCode
* Visit [https://code.visualstudio.com/](https://code.visualstudio.com/) to install Visual Studio Code
* Follow the provided installation instructions to complete installation
* Once Visual Studio Code has finished installation you should be able to see a screen similar to this and have successfully installed VSCode
![VsCode](https://user-images.githubusercontent.com/97651048/149445811-b387faf3-4e73-4be4-a44b-ff01794d1153.PNG)

---
## Remotely Connecting
* Find your course-specifc account for CSE15L at [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php)
* Open a terminal in VSCode and enter ```ssh cs15lwi22zz@ieng6.ucsd.edu``` (Remember to replace `zz` with the phrase in your account) and type yes to connect to a server at the CSE Basement
* After entering your password, output to the terminal should look like this
![Image 2](https://user-images.githubusercontent.com/97651048/149445831-4cf1a218-3124-4955-a68a-8561a1265e3a.PNG)

---
## Trying Some Commands
Experiment with the commands given to see what they do
* `cd` - change directory
* `ls -lat` - list files
* `cd ~` - change directory to home folder
Heres an example
![Image 3](https://user-images.githubusercontent.com/97651048/149446900-da2685c3-49bf-4bcf-b88f-f53afb7c513c.PNG)

---
## Moving Files With `scp`
* `scp` is a command to move files from your computer to the remote computer
* Use the provided code to create a java file named `ScpCommand.java`
``` class ScpCommand {
    public static void main(String[] args) {
      System.out.println("Hello my Operating System is " + System.getProperty("os.name"));
      System.out.println("My name is " + System.getProperty("user.name"));
    }
  }
```
* Run the file with `javac` and `java` to see what you get then move the file to the remote computer with `scp ScpCommand.java cs15lwi22zz@ieng6.ucsd.edu:~/` (Change the zz to the phrase in your account). After it transfers, try signing in to the remote server and running it again to see if you get something similar to this


