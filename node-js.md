# Node.js Basics

## Notes

21.03.30.

### General

What it's not? It'not a language, a framework or a library.\
What is it? “Node.js is a JavaScript runtime built on the Chrome V8 JavaScript engine.” It basically means, that Node.js lets us run JavaScript programs.

### Installation

We have to run the following in the Terminal:

`sudo apt-get install node.js`

Then we can check if it's installed, to see the version number:

`node -v`

### Executing .js

We have to cd to the desired directory, then type:

`node program.js`

### Debugging/inspecting a script

The former `node debug` command is deprecated and we can inspect a script, by typing:

`node inspect program.js`

We exit the debugger by pressing "Ctrl+C" twice or typing ".exit".