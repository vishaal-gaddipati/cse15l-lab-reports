# **Lab Report 1 - Week 2**
## Tutorial for incoming 15L students about how to log into a course-specific account on *ieng6*.

---
### **Step 1 - Installing VScode**
Install Visual Studio Code from the website [https://code.visualstudio.com/](https://code.visualstudio.com/) by clicking the download button for your specfic operating system. Download the setup file and follow the steps to install VSCode on your system.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/vscode.jpg?raw=true)

---
### **Step 2 - Remotely Connecting**
If you are on Windows install [OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse). Search for your personal course specific account for CSE15L [here](https://sdacs.ucsd.edu/~icc/index.php). Next in Visual Studio Code open a terminal (Ctrl + ` or click the Terminal dropdown then New Terminal). Then with your course-specific account in the format cs15lsp22zz@ieng6.ucsd.edu, replacing zz with your course account username, follow the ssh command in the image below making sure to type in your password.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/remoteconnect.jpg?raw=true)

---
### **Step 3 - Trying Some Commands**
Now that you are logged in, try some commands like **cd**, **ls**, **pwd**, **mkdir**, and **cp** in the terminal. Try these in a terminal on your own computer and in the remote terminal and compare the outputs. Try these commands as well...
```
cd ~
cd
ls -lat
ls -a
ls <directory>
cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/
cat /home/linux/ieng6/cs15lsp22/public/hello.txt
```
Here is an example of a command being run in the SSH terminal:

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/commandEx.jpg?raw=true)

---
### **Step 4 - Moving Files with scp**
We will now use the command **scp** from the *client* (your computer, not logged into ieng6). Create a file titled **WhereAmI.java** and copy paste this code into it:
```
class WhereAmI {
    public static void main(String[] args) {
        System.out.println(System.getProperty("os.name"));
        System.out.println(System.getProperty("user.name"));
        System.out.println(System.getProperty("user.home"));
        System.out.println(System.getProperty("user.dir"));
    }
}
```
In the terminal within the directory where you made the file and run this command with your username:
>scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/

Log into ieng6 and run the program using **javac** and **java** to see that the copy completed.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/scpEx.jpg?raw=true)

---
### **Step 5 - Setting an SSH Key**
To prevent having to type a password each time **ssh** or **scp** are used we can utilize a program called **ssh-keygen**. Here is what you should type to set it up:
```
# on client (your computer)
$ ssh-keygen
/Users/<user-name>/.ssh/id_rsa
Hit enter twice

$ ssh cs15lsp22ack@ieng6.ucsd.edu
<Enter Password>

# now on server
$ mkdir .ssh
$ <logout>

# back on client
$ scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys

# do this using your username and the path you saw in the command above
```
Now you should be able to log in with **ssh** or use **scp** with no password like in the image below.

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/keygen.jpg?raw=true)

---
### **Step 6 - Optimizing Remote Running**
In order to make running commands more pleasant and optimized it is good to learn some common shortcuts. You can run a command at the end of an ssh command by typing it in quotes, like **"ls"**, which will log in, run the command on the server, then exit. Placing multiple commands on one line can be accompished using semicolons and the up-arrow on the keyboard recalls the previous command that was run. Here is an example of some shortcuts being used together:

![Image](https://github.com/vishaal-gaddipati/cse15l-lab-reports/blob/main/optimizing.jpg?raw=true)