# **Lab Report 2 - Week 4**
## In this lab report I will show 3 code changes to a Markdown parser implementation for web links that prevents some bugs and their symptoms based on failure-inducing inputs.

### **Change #1**
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%202/noBracketFix.jpg?raw=true)

Test file for *failure-inducing input* that prompted the change:
> [test-file2.md](https://github.com/vishaal-gaddipati/markdown-parser/blob/main/test-file2.md?plain=1)

The *symptom* of that failure-inducing input:
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%202/noBracketError.jpg?raw=true)

The failure-inducing input was a Markdown file without brackets which created the symptom of an infinite loop. The bug in the code that created the symptom was that there was no if statements that checked whether or not brackets existed in the String being parsed. If there are no open or closed brackets, then the while loop must break as those are not valid link formats for the parser.

---
### **Change #2**
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%202/noParenFix.jpg?raw=true)

Test file for *failure-inducing input* that prompted the change:
> [test-file7.md](https://github.com/vishaal-gaddipati/markdown-parser/blob/main/test-file7.md?plain=1)

The *symptom* of that failure-inducing input:
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%202/noParenError.jpg?raw=true)

The failure-inducing input was a Markdown file without parentheses which created the symptom of an out of bounds error. The bug in the code that created the symptom was that there was no if statements that checked whether or not parentheses existed in the String being parsed. If there are no open or closed parentheses, then the while loop must break as those are not valid link formats for the parser.

---
### **Change #3**
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%202/imageFix.jpg?raw=true)

Test file for *failure-inducing input* that prompted the change:
> [test-file9.md](https://github.com/vishaal-gaddipati/markdown-parser/blob/main/test-file9.md?plain=1)

The *symptom* of that failure-inducing input:
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%202/imageError.jpg?raw=true)

The failure-inducing input was a Markdown file with an image link which created the symptom of wrong output, because "page.com" should not be printed. The bug in the code that created the symptom was that there was no if statement that checked whether or not an exclamation point existed in the String being parsed. If there is an exclamation point, then the image link must be skipped before the rest of the links are added as images are not valid link formats for the website URL parser.