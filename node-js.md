# Node.js Basics

## Q & A

Q1: What is Node.js?\
A1: An open-source, cross-platform, back-end JavaScript runtime environment. It runs on the V8 engine and executes code outside a web browser.

Q2: What is a runtime system/environment?\
A2: It is a place, where a program or application is executed. The hardware and software infrastructure that supports the running of a particular codebase in real life.

Q3: How can we run JS files in CLI?\
A3: With Node.js, using the "node program.js" command.

Q4: What is the inspect command used for?\
A4: We can debug our code with the help of that command.

Q5: How do we exit the inspector?\
A5: By pressing "Ctrl+C" twice or typing ".exit". 

## Notes

### General

What it's not? It's not a language, a framework or a library.\
What is it? “Node.js is a JavaScript runtime built on the Chrome V8 JavaScript engine.” Meaning, Node.js lets us run JavaScript programs.

### Installation

We have to run the following in the Terminal:

`sudo apt-get install node.js`

Then we can check if it's installed, to see the version number:

`node -v`

### Executing .js

We have to cd to the desired directory, then type:

`node program.js`

### Debugging/inspecting a script

The former `node debug` command is deprecated and we can inspect a script by typing:

`node inspect program.js`

We exit the debugger by pressing "Ctrl+C" twice or typing ".exit".