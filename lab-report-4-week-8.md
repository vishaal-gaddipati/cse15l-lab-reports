# **Lab Report 4 - Week 8**
## In this lab report I will show tests being run on 2 different markdown parser implementations with 3 snippets.

Here is my repository:
[https://github.com/vishaal-gaddipati/markdown-parser](https://github.com/vishaal-gaddipati/markdown-parser)

Here is the one I reviewed in Week 7:
[https://github.com/calistajlee/lab6-markdown-parser](https://github.com/calistajlee/lab6-markdown-parser)

### **Test for Snippet 1**
Snippet 1 should produce the output:

```
[url.com, google.com, google.com, ucsd.edu]
```

Here is the test I created below.
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%204/snippet1Test.jpg?raw=true)

Here is the output for my implementation.
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%204/myOutput1.jpg?raw=true)

Here is the output for the implementation I reviewed in Week 7.
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%204/otherOutput1.jpg?raw=true)

I think the code change that would make the program work for snippet 1 would be to utilize a different target for the string search that uses something other than brackets or parentheses. This could be looking for a "." in each url possibly for the string. This is a more involved change however, as the whole method would need to be overhauled.

---
### **Test for Snippet 2**
Snippet 2 should produce the output:

```
[a.com, b.com, a.com, example.com]
```

Here is the test I created below.
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%204/snippet2Test.jpg?raw=true)

Here is the output for my implementation.
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%204/myOutput2.jpg?raw=true)

Here is the output for the implementation I reviewed in Week 7.
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%204/otherOutput2.jpg?raw=true)

I think the code change that would make the program work for snippet 2 would be to utilize a different target for the string search that uses something other than brackets or parentheses, which is the same exact solution for snippet 1. This could be looking for a "." in each url possibly for the string. This is a more involved change however, as the whole method would need to be overhauled.

---
### **Test for Snippet 3**
Snippet 3 should produce the output:

```
[https://www.twitter.com, https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule, https://cse.ucsd.edu/]
```

Here is the test I created below.
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%204/snippet3Test.jpg?raw=true)

Here is the output for my implementation.
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%204/myOutput3.jpg?raw=true)

Here is the output for the implementation I reviewed in Week 7.
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%204/otherOutput3.jpg?raw=true)

I think the code change that would make the program work for snippet 3 would be to ignore the line breaks. This could be looking for a "." in each url possibly. This is a more involved change however, as the whole method would need to be overhauled.