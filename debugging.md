# Debugging

## Q&A

Q1: Why is Call Stack important?\
A1: It's fundamental to how JS works and it's helpful for debugging. It does also come up in interviews.

Q2: What is Call Stack?\
A2: It's like a "todo list" of function invocations. A structure that stores/keeps track of the history of things (like a list of what is) waiting to be returned. 

## Notes

21.04.11.

### Call Stack

"A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc."

Last In, First Out data structure.

- Frames are arranged in a **stack**. The frame for the most-recently called function is always on the top.
- When a new function is called, a new frame is **pushed** onto the top of the stack and becomes the active frame.
- When a function finishes its work, its frame is popped off of the stack and the frame below becomes the new, active function on the top. This funciton picks up immediately where it left off.

Stack Definition
- An ordered set of stack frames
- Most recently invoked function is on the top of the stack
- The bottom of the stack is the first function invoked
- The stack is processed from top to bottom

### UML Sequence diagram

Shows the sequence of events.

Sequence diagrams are a type of UML diagram, that shows how objects in a system or classes within code interact with eachother.