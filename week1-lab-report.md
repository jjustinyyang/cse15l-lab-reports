Week 1 Lab Report
---
In this week's lab, we are going to install VSCode which is what we are going to use in this course as a code editor. 
We are also going to remotely connecting our personal computer to the school's server computer using our course-specific account. 
After that, we can play around with different commands using the VScode terminal.

Installing VScode
---
To install VScode, go to the following website, [https://code.visualstudio.com/](https://code.visualstudio.com/).

There should be the version for most common operating systems (macOS and Windows).

Follow the instruction given from it after.

VScode should look like something like this once installed: <br>
![image](installing_vscode.png)

Remotely Connecting
---
Before attempt remotely connecting your computer to school server, you will need to know your course-specific account for CSE15L.

Go to this [link](https://sdacs.ucsd.edu/~icc/index.php).

Open VScode terminal: Terminal > New Terminal.

Type into terminal: `ssh` following your course-specific account.

You should be prompt with your password.

After comfirming correct password, you are logged in remotely connecting with the school server: <br>
![image](remotely_connecting.png)

Trying Some Commands
---
Try getting some practice with typing commands in the terminal. 

Ex: <br>
`cd ~` <br>
`ls -lat` <br>
`ls /home/linux/ieng6/cs15lwi23/cs15lwi23abc (replace abc with a groupmate's username)` <br>
`cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/` <br>
`cat /home/linux/ieng6/cs15lwi23/public/hello.txt`

![image](trying_some_commands.png)
