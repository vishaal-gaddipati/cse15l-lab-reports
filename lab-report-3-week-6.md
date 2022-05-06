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