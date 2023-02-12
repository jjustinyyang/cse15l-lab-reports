Part 1
---

This is the code for my string server:

![Image](string-server-code.png)

This is what I type in as URL to get the first string printed:

![Image](hello.png)

StringServer.java above calls the Handler class which in turn calls the public method handleRequest where the argument is the URL of the server. By having the proper format for adding a string, `/add-message?s=<string>`, the URL handler then splits the query by “=” into an array where second half stores the actual message. This message is added to the arraylist that I created and eventually using a for-loop, printing the strings in the arraylist in order with a line in bewteen.

Adding another string:

![Image](world.png)

This time, there is a word in the arraylist which is "hello". The same process happens with the Handler class and handleRequest method taking in the URL argument. Again, with proper format for adding string, it goes through the process of splitting the query with 0th as a checker index which the string has to equal "s" and 1st as where the actaul string message locates. The string "world is added to the arraylist and with the help of the for-loop, prints out the messages in the arraylist in order of adding with a new line after each onto the server.

Part 2
---

A failure-inducing input for the buggy program:

```
@Test
public void testReverseInPlace() {
    int[] input2 = { 1, 2, 3 };
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{ 3, 2, 1 }, input2);
}
```

A failing JUnit test: 

![Image](bad-input.png)

When I have the input array of `{1, 2, 3}`, I would expect the `reverseInPlace()` to reverse the array and return the array `{3, 2, 1}`. This induced an error because the actual output was instead remained the same as `{1, 2, 3}`.

An input that doesn’t induce a failure:

```
@Test
public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
}
```

A passing JUnit test: 

![Image](good-input.png)

The input array of only one element such as `{3}` will not induce a failure because there is only one element, the symptom of not reversing the array does not affect the output in this case.

Notice how a buggy program can sometime still result in a passing test depends on your input, so that is the reason why we need to write tests addressing different inputs to find the bug in the program.

The symptom is that they return the same array even though I expected an reversed array.

The failing result of JUnit test:

![Image](bad-input.png)

![Image](lab3-symptom.png)

We can see that with both the good and bad input, it errored on the second one as it didn't correctly reverse the array.

There are two bugs I found that caused the same symptom of not reversing the array:
- It only copies one side to the other, when what we want is actually swapping the front and the end.
- The for-loop looped through the entire array when instead it should only be half of the array because if you loop through the entire it would just counter the swap and resulting in the same array.

Before fix:

```
static void reverseInPlace(int[] arr) {
    for (int i = 0; i < arr.length; i += 1) {
        arr[i] = arr[arr.length - i - 1];
    }
}
```

After fix:

```
static void reverseInPlace(int[] arr) {
    for (int i = 0; i < arr.length / 2; i += 1) {
        int temp = arr[i];
        arr[i] = arr[arr.length - i - 1];
        arr[arr.length - i - 1] = temp;
    }
}
```

Notice that now the array is looped to the middle of the array and swapping the elements of the front and its corresponding end indexes.

Part 3
---

Something I learned from lab in week 2 and 3 that you didn’t know before is the stucture of URL's. I learned the meanings of different sections of the long chain of letters, slashes, and different symbols. I learned what domain, path, query, and fragment are, and what information they provide. I learned to use them in couple practice such as the number counter, search engine, and string appender.
