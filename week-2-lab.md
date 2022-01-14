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
``` 
class ScpCommand {
    public static void main(String[] args) {
      System.out.println("Hello my Operating System is " + System.getProperty("os.name"));
      System.out.println("My name is " + System.getProperty("user.name"));
    }
  }
```
* Run the file with `javac` and `java` to see what you get then move the file to the remote computer with `scp ScpCommand.java cs15lwi22zz@ieng6.ucsd.edu:~/` (Change the zz to the phrase in your account). After it transfers, try signing in to the remote server and running it again to see if you get something similar to this
![Image 4](https://user-images.githubusercontent.com/97651048/149448776-6893ebd5-5627-4396-a0c2-84872e49fb6f.PNG)



---
## Setting an SSH Key
* Instead of having to enter a password every time to run commands to a remote server, you can instead generate ssh keys to skip this step
* Follow the commands to set this up
* Make a .ssh directory

![Capture 1](https://user-images.githubusercontent.com/97651048/149584240-fdd2f145-1261-4aa9-9bba-7e9662439f85.PNG)

* Create a SSH Key from your computer 

![Capture 2](https://user-images.githubusercontent.com/97651048/149584135-0f7d95ac-ebbb-4a09-8b37-caa7743f14ce.PNG)

* Run these commands if your Operating System is Windows

![Capture 3](https://user-images.githubusercontent.com/97651048/149584211-ece4ad85-7a07-4da9-9a49-cd94316a3290.PNG)

* `scp` the file over to the remote server and now you can run commands without logging in

![Capture 4s](https://user-images.githubusercontent.com/97651048/149584499-96fa93a6-fa7b-49d7-a5c1-7f1542ec1c9b.png)



---
## Optimizing Remote Running
* Writing a command in quotes will allow the command to run directly on the remote server
* Semicolons can also be used to run multiples commands in a singular line
Heres an example



