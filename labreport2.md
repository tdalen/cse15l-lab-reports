# Lab Report 2: Servers and Bugs
## Part 1
**`StringServer` code:**

<img src="https://github.com/tdalen/cse15l-lab-reports/blob/main/StringServerCode.png?raw=true" width="50%" height="50%">

**Using `/add-message`:**

<img src="https://github.com/tdalen/cse15l-lab-reports/blob/main/hello.png?raw=true" width="50%" height="50%">

For this output, the `main` method in the `StringServer` class is run, which starts a server using port 3041. The `handleRequest` method in the `Handler` class is also run, which filters through the different cases depending on what arguments are passed as the path. For this example, the argument for the path was `/add-message` and the argument for the query was `?s=Hello`. The class variable `current` was initially `""` (empty string), but after running `handleRequest` with those arguments, `current`'s value was updated to `"Hello"` with a newline after.

<img src="https://github.com/tdalen/cse15l-lab-reports/blob/main/howareyou.png?raw=true" width="50%" height="50%">

For this output, the server was already started through the `main` method from the previous example. The `handleRequest` method is run again since the query changed. The argument for the path was `/add-message` and the argument for the query was `?s=How are you`. Passing these arguments updated `current` from `"Hello" + "\n"` to `"Hello + "\n" + "How are you" + "\n"`. This prints out:
```
Hello
How are you
```

## Part 2

## Part 3
In Weeks 2 and 3, I learned a lot about URLs and the different parts of a URL that I didn't know before. I've always heard the term URL, but never learned what exactly it was or how to work with URLs in code until these two weeks. I now know about the different parts that make up a URL, like paths, queries, and fragments, and what purpose each of them serve. I also learned about the URI class in Java that allows us to work with creating and reading URLs.
