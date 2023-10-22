# A Beginners Guide To Ctf's
**picoCTF: The Webshell**
To access the picoCTF webshell click webshell in the corner of the screen.
![Click This Button](https://i.imgur.com/nW8vxLJ.png)
Then you will see this screen:
![enter image description here](https://i.imgur.com/OmSxaGQ.png)
There are many different things you can do with this web terminal. (Linux)
[This Challenge](https://play.picoctf.org/practice/challenge/170) is a good example of using it. Here is the writeup for that:
Question: Can you invoke help flags for a tool or binary?  [This program](https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm)  has extraordinarily helpful information…

Files: warm

Approach: After downloading the file running the command

> file warm

shows it as an executable file.

When we try to run using

> ./warm

It gives error. One of the reason might be that it does not have execution permission. To give permission enter

> chmod +x warm

running again gives

Hello user! Pass me a -h to learn what I can do!

Finally running

> ./warm -h

returns the flag

Flag: picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}

You can run file like this but to run Python (.py) you have to do something different.

**Python**

Python in the picoCTF terminal is preinstalled. To find out all commands do `$ man python`. This will list all commands. Here are the most helpful:

*(Delete the brackets)*
  `ls` Will list all files in your directory.
  `wget [url]` This will import your file into the terminal.
  `python [file]` Will run a file in your directory
 >**A good example of these is [this challenge.](https://play.picoctf.org/practice/challenge/166?page=1)**
 >- `python [file] -e [file.txt]` Will encrypt a file with the python script.
 >- `python [file] -d [file.txt]` Will decrypt a file with the python script.
 - `python [file]` Will run a python file.
 
Here is an example of some of these commands:
![enter image description here](https://i.imgur.com/AWMV2EM.png)
 
**Best programs on the terminal**
 1. Gobuster
 >Gobuster is a web exploitation program that searches for open ports. You can install it on mac with [Homebrew](https://formulae.brew.sh/formula/gobuster). Install it on linux 
 3. 
