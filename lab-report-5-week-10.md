# **Lab Report 5 - Week 10**
## This lab report will cover the different implementations of markdown parser with various tests. The tests that I found with different results were obtained from a vimdiff command call.

### **The two tests are:**

[494.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/494.md)

[530.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/530.md)

The command:
```
vimdiff my-markdown-parser/results.txt cse15lsp22-markdown-parser/results.txt
```
---

### **494.md**
The implementation that is correct is the provided markdown parser and not mine. The issue with my implementation is that there is a parenthesis missing.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%205/494.jpg?raw=true)

The expected output is:
```
[\foo\)]
```
The underlying issue with my code is that after it finds a closed parenthesis, it stops looking beyond that point within the link. It should continuing looking until the *last* closing parenthesis if found. It could be implemented in this area below.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%205/myError.jpg?raw=true)

### **530.md**
The implementation that is correct is my implementation of the parser and not the provided one. The issue with the given parser is that it does not ignore images.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%205/530.jpg?raw=true)

The expected output is:
```
[]
```
The underlying issue with the given code is that it does not skip images, which are very similar to links apart from the exclamation point. The solution would be that if there was an exclamation point, it should skip the image and move to the next link.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%205/excPointCheck.jpg?raw=true)