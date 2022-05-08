# **Lab Report 3 - Week 6**
## In this lab report I will show all 3 Group Choice options from Lab 5.

### **Group Choice 1 - Streamlining *ssh* Configuration**
The first option is Streamline ssh Configuration. Creating a configuration file saves some typing by telling SSH what username to utilize when logging onto the server. The entry itself is located in *~/.ssh/config*.

Here is the *.ssh/config* file, and how I edited it with Notepad.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%203/configFile.jpg?raw=true)

This image below shows how using the *ssh* command looks when logging into my account simply using the alias ieng6 instead of the following line of long code:
```
$ ssh cs15lsp22ack@ieng6.ucsd.edu
```

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%203/sshLogin.jpg?raw=true)

Even the *scp* command is quicker to type utilizing the alias I put into the config file. It copies a java file to the ieng6 server in fewer characters.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%203/scpAlias.jpg?raw=true)

---
### **Group Choice 2 - Setup Github Access from ieng6**
The second option is Set up Github Access from ieng6. Copying a public key from ssh-keygen to Github from my course-specific account allows for me to push to Github from the *ieng6* machines.

This is where the public key I made is stored on Github in my user account.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%203/pubKey.jpg?raw=true)

The private key is stored here in my user account.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%203/privKey.jpg?raw=true)

Here is the *git* commands being run while being logged into the ieng6 account. A commit is made and it is pushed to Github.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%203/gitCom1.jpg?raw=true)
![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%203/gitCom2.jpg?raw=true)

Here is the [commit](https://github.com/vishaal-gaddipati/markdown-parser/commit/adbff963a92c77412b72e5c87a3a06d375ceac29):

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%203/resulCom.jpg?raw=true)

---
### **Group Choice 3 - Copy whole directories with *scp -r***
The third option is Copy Whole Directories with *scp -r*. Running the *scp -r* commands allows for an entire directory to be copied saving time from copying each individual file.

Here is the whole markdown-parse directory being copied to my ieng6 account.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%203/copyDir.jpg?raw=true)

Here is the tests being compiled and run in the directory that was just copied into my ieng6 account.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%203/iengRun.jpg?raw=true)

The long line of code below combines *scp*, *;*, and *ssh* to copy the whole directory and run the tests in one line.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/Screenshots/Lab%203/combinedRun.jpg?raw=true)