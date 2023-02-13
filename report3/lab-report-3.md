In this lab report I am going to research on the `grep` command line options. Examples of them would be provided using the files and directories from `./written_2` provided in class.

`grep -w <string> <path/to/file>`
---

This command line option helps you search for a specific word with out giving you words that contains the word you are searching for.

For example, you want to find the word "the", words like "then" or "they", any words containing "the" as part of their word is going to match. With this command line option, it will only give you lines containing "the".

Example 1:

![Image](grep-w1.png)

I wanted try find the word "survey" in the `Canada-WhereToGo.txt` file. However, it is giving me paragraphs (technically lines because grep thinks a paragraph as a line) with the word "surveyors". On the bottom, I uses the command line option `-w` to limiting only to the word "survey", and not others containing it. Notice there is less printed out.

Example 2:

![Image](grep-w2.png)

I want the search the word "marriage", it gives me line with the word "marriageable". With `-w` it shows no results meaning there is no word as "marriage" in the passage.

`grep [<list or range of letters>] <path/to/file>`
---

I created a text file containing all the paths with file names containing "WhereToGo" for easier demonstrating this command line option with examples. I stick to [<list of letters>] for my examples, such as [aeiou]. While it can also be [<range of letters>], like [a-e], which search for a, b, c, d, and e. However, it is hard to find a range of letter using the text file as the path contains most of the letters and I don't want it to return every line. 

Example 1:

![Image](greplist1.png)

I want to look for lines that contains letters c, f, or j, and as shown above, I can do it with this specific command line option.

Example 2:

![Image](greplist2.png)
  
Same as above example, this time look for letters k, p, or q. 

`grep ^<string> path/to/file`
---

Example 1:

![Image](grep^1.png)

Example 2:

![Image](grep^2.png)

`grep -i <string> <path/to/file>`
---

Example 1:

![Image](grep-i1.png)

Example 2:

![Image](grep-i2.png)
