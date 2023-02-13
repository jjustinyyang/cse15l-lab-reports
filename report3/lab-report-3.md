In this lab report I am going to research on the `grep` command line options. Examples of them would be provided using the files and directories from `./written_2` provided in class.

`grep -w <string> <path/to/file>`
---

This command line option helps you search for a specific word with out giving you words that contains the word you are searching for.

For example, you want to find the word "the", words like "then" or "they", any words containing "the" as part of their word is going to match. With this command line option, it will only give you lines containing "the".

![Image](grep-w1.png)

![Image](grep-w2.png)

`grep [<list or range of letters>] <path/to/file>`
---

![Image](greplist1.png)

![Image](greplist2.png)

`grep ^<string> path/to/file`
---

![Image](grep^1.png)

![Image](grep^2.png)

`grep -i <string> <path/to/file>`
---

![Image](grep-i1.png)

![Image](grep-i2.png)
