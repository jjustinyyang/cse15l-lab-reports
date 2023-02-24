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
`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`
`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`

[!image](fail_tests.png)

(7) Edit the code file to fix the failing test
---

[!image](fix.png)

(8) Run the tests, demonstrating that they now succeed
---
[!image](succeed_tests.png)

(9) Commit and push the resulting change to your Github account
---
[!image](commit_push.png)
