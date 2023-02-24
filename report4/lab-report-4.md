Tasks From Competition
---
1. Setup Delete any existing forks of the repository you have on your account
2. Setup Fork the repository
3. The real deal Start the timer!
4. Log into ieng6
5. Clone your fork of the repository from your Github account
6. Run the tests, demonstrating that they fail
7. Edit the code file to fix the failing test
8. Run the tests, demonstrating that they now succeed
9. Commit and push the resulting change to your Github account

(1) Setup Delete any existing forks of the repository you have on your account
---
If previously forked the repository, delete it to ensure fairness of competition.

Inside the repository, go to Setting --> Danger Zone --> Delete this repository

Read the warning, type the name of the repository you want to delete to verify deleting the correct repository.

[!image](delete_repo.png)

(2) Setup Fork the repository
---
Fork the [lab 7 repository](https://github.com/ucsd-cse15l-w23/lab7).

[!image](fork_repo.png)

(3) The real deal Start the timer!
---
Phone, on-line, or any timer.

[!image](timer.png)

(4) Log into ieng6
---
Log into remote server `ieng6`.

Type into terminal command line: `ssh cs15lwi23auv@ieng6.ucsd.edu`

It should not prompt for password after the set up I did in class today.

[!image](login.png)

(5) Clone your fork of the repository from your Github account
---
Clone the repository I forked using command line: `git clone https://github.com/jjustinyyang/lab7.git`

[!image](clone_repo.png)

(6) Run the tests, demonstrating that they fail
---
`cd` (change directory) into the folder created after cloning: `cd lab7`

Inside the folder, compile all java files and run junit on the test file `ListExamplesTests.java`:

`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`

and

`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`

There is an error that we need to fix!

[!image](fail_tests.png)

(7) Edit the code file to fix the failing test
---

When we open the `ListExamplesTests.java` file on Github, we can see that the test methods only run for merge1 method, so we can focus on that method to find the bug in it.

[!image](nano.png)

[!image](before_fix.png)

[!image](after_fix.png)

(8) Run the tests, demonstrating that they now succeed
---
Do the steps in step 6, which this time, we are already inside lab7 folder so no need to `cd` into it.

This time, it should pass all the tests.

[!image](succeed_tests.png)

(9) Commit and push the resulting change to your Github account
---
`git status`

`git add`

`git commit -m <message>`

`git push`

[!image](commit_push.png)
