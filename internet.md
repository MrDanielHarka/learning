# The Internet

## Q & A

Q1: What are HTTP & DNS used for?\
A1: Used and responsible for sending and receiving web files.

Q2: What is TCP/IP & Routing used for?\
A2: Used for braking down and transporting packets.

Q3: What are the 4 main HTTP request modes and what are they for?\
A3: 1. GET used to read/retrieve a representation of a source. It returns in XML or JSON. 2. POST used to create new resources. Carries payload that specifies the data for the new resource. 3. PUT utilized for update capabilities. Payload may contain updated data for the resource. 4. DELETE used to delete a resource identified by a URI.

Q4: What is the difference between TCP and UDP?\
A4: TCP is a connection-oriented protocol, whereas UDP is a connectionless protocol.

Q5: What are HTTP status codes used for?\
A5: Tells us if an HTTP request has been successfully completed.

Q6: What information can we obtain from Chrome Devtools if we would like to inspect the HTTP Requests/Responses?\
A6: It can shows us how many Requests/Responses we get and how long did they take and if there were any errors.

Q7: What is minification?\
A7: It is when we remove all unnecessary characters from our code (such as whitespace, line breaks, commments), so that it would have smaller size and would be transferred much faster.

Q8: What is the OSI Model?\
A8: It desribes the 7 layes that computer systems use, to communicate over a network. 

Q9: What is REST?\
A9: An architectural style for providing standards between computer systems on the web. Makes it easier for systems to communicate with each other.

## Notes

### The Internet Layers

- HTTP & DNS: Manage the sending and receiving of web files.
- TCP/IP & Routing: Break down and transport packets.
- Wires, cables & Wifi: Binary sequences of 1's & O's are sent physically.

### HTTP (Hypertext Transfer Protocol)

- Allows communication between hosts and clients.
- Supports a mixture of network configurations.
- Communicating on request/response pair.

### The URL (Uniform Resource Locator)

- The way of sending request messages.
- Components:
    - Protocol: Typically http or https.
    - Port: Default is 80, but can be set explicitly.
    - Local path: Resource on the server.

### Verbs

- "The action that should be performed on the host is specified via HTTP verbs.""
- Most common request verbs:
    - GET: fetch an existing resource. URL contains all necessary info the server needs to locate and return the resource.
    - POST: create a new resource. Usually carries payload that specifies the data for the new resource.
    - PUT: update an existing resource. Payload may contain the updated data for the resource.
    - DELETE: delete an existing resource.
- Less commong verbs that HTTP also supports:
    - HEAD: this is similar to GET, but without the message body. It's used to retrieve the server headers for a particular resource, generally to check if the resource has changed, via timestamps.
    - TRACE: used to retrieve the hops that a request takes to round trip from the server. Each intermediate proxy or gateway would inject its IP or DNS name into the Via header field. This can be used for diagnostic purposes.
    - OPTIONS: used to retrieve the server capabilities. On the client-side, it can be used to modify the request based on what the server can support.

### TCP vs UDP:

- TCP is a connection-oriented protocol, whereas UDP is a connectionless protocol.
- The speed for TCP is slower while the speed of UDP is faster
- TCP uses handshake protocol like SYN, SYN-ACK, ACK while UDP uses no handshake protocols
- TCP does error checking and also makes error recovery, on the other hand, UDP performs error checking, but it discards erroneous packets.
- TCP has acknowledgment segments, but UDP does not have any acknowledgment segment.
- TCP is heavy-weight, and UDP is lightweight.


### Status Codes

**General**

HTTP response status codes indicate whether a specific HTTP request has been successfully completed.

Responses are grouped in five classes:
- Informational responses (100–199)
- Successful responses (200–299)
- Redirects (300–399)
- Client errors (400–499)
- Server errors (500–599)

**1xx: Informational Messages**

The server can send a Expect: 100-continue message, telling the client to continue sending the remainder of the request, or ignore if it has already sent it.

**2xx: Successful Responses**

200 OK:
The request has succeeded. The meaning of the success depends on the HTTP method:
- GET: The resource has been fetched and is transmitted in the message body.
- HEAD: The entity headers are in the message body.
- PUT or POST: The resource describing the result of the action is transmitted in the message body.
- TRACE: The message body contains the request message as received by the server.

201 Created:
The request has succeeded and a new resource has been created as a result. This is typically the response sent after POST requests, or some PUT requests.

There are others, but less common.

**3xx: Redirection Messages**

300 Multiple Choice:
The request has more than one possible response. The user-agent or user should choose one of them. (There is no standardized way of choosing one of the responses, but HTML links to the possibilities are recommended so the user can pick.)

301 Moved Permanently:
The URL of the requested resource has been changed permanently. The new URL is given in the response.

302 Found:
This response code means that the URI of requested resource has been changed temporarily. Further changes in the URI might be made in the future. Therefore, this same URI should be used by the client in future requests.

303 See Other:
The resource is temporarily located at a new URL. The Location response header contains the temporary URL.

304 Not Modified:
The server has determined that the resource has not changed and the client should use its cached copy. This relies on the fact that the client is sending ETag (Enttity Tag) information that is a hash of the content. The server compares this with its own computed ETag to check for modifications.

There are others, but those are less common.

**4xx: Client Error Responses**

400 Bad Request:
The server could not understand the request due to invalid syntax.

401 Unauthorized:
Although the HTTP standard specifies "unauthorized", semantically this response means "unauthenticated". That is, the client must authenticate itself to get the requested response.

402 Payment Required 
This response code is reserved for future use. The initial aim for creating this code was using it for digital payment systems, however this status code is used very rarely and no standard convention exists.

403 Forbidden:
The client does not have access rights to the content; that is, it is unauthorized, so the server is refusing to give the requested resource. Unlike 401, the client's identity is known to the server.

404 Not Found:
The server can not find the requested resource. In the browser, this means the URL is not recognized. In an API, this can also mean that the endpoint is valid but the resource itself does not exist. Servers may also send this response instead of 403 to hide the existence of a resource from an unauthorized client. This response code is probably the most famous one due to its frequent occurrence on the web.

There are others, but those are less common.

**5xx: Server Error Responses**

500 Internal Server Error:
The server has encountered a situation it doesn't know how to handle.

501 Not Implemented:
The request method is not supported by the server and cannot be handled. The only methods that servers are required to support (and therefore that must not return this code) are GET and HEAD.

502 Bad Gateway:
This error response means that the server, while working as a gateway to get a response needed to handle the request, got an invalid response.

503 Service Unavailable:
The server is not ready to handle the request. Common causes are a server that is down for maintenance or that is overloaded. Note that together with this response, a user-friendly page explaining the problem should be sent. This responses should be used for temporary conditions and the Retry-After: HTTP header should, if possible, contain the estimated time before the recovery of the service. The webmaster must also take care about the caching-related headers that are sent along with this response, as these temporary condition responses should usually not be cached.

504 Gateway Timeout:
This error response is given when the server is acting as a gateway and cannot get a response in time.

There are others, but those are less common.

### Cookies vs. localStorage vs. sessionStorage

**General**

In all cases, these storage mechanisms will be specific to an individual browser on an individual computer/device. Any requirement to store data on an ongoing basis across sessions will need to involve application server side - most likely using a database, but possibly XML or a text/CSV file. localStorage, sessionStorage, and cookies are all client storage solutions. Session data is held on the server where it remains under your direct control.

**localStorage**

Pros:
- Stores data with no expiration date.
- Storage limit is about 5MB.
- Data is never transferred to the server.
Cons:
- Plaintext, hence not secure by design.
- Limited to string data, hence need to be serialized.
- Can only be read on client-side.

**sessionStorage**
- Stores data only for a session, meaning that the data is stored until the browser (or tab) is closed.
- Data is never transferred to the server.
- Can only be read on client-side.
- Storage limit is about 5-10MB.
- Opening multiple tabs/windows with the same URL creates sessionStorage for each tab/window.

**Cookie**

- Stores data that has to be sent back to the server with subsequent XHR requests. Its expiration varies based on the type and the expiration duration can be set from either server-side or client-side.
- Cookies are primarily for server-side reading (can also be read on client-side), localStorage and sessionStorage can only be read on client-side.
- Size must be less than 4KB.
- Cookies can be made secure by setting the httpOnly flag as true for that cookie. This prevents client-side access to that cookie.

![alt text](https://miro.medium.com/max/700/1*dMoXCZgsdlQoSITo5BdXoA.png "Cookies vs. localStorage vs. sessionStorage")

### Minification

"Minification (also minimisation or minimization) is the process of removing all unnecessary characters from the source code of interpreted programming languages or markup languages without changing its functionality. These unnecessary characters usually include white space characters, new line characters, comments, and sometimes block delimiters, which are used to add readability to the code but are not required for it to execute. Minification reduces the size of the source code, making its transmission over a network (e.g. the Internet) more efficient."

### The 7 layers of the OSI model

- Layer 7 - Application: The one at the top. It’s what most users see. In the OSI model, this is the layer that is the “closest to the end user”.
- Layer 6 - Presentation: It represents the preparation or translation of application format to network format, or from network formatting to application format. “Presents” data for the application or the network. A good example of this is encryption and decryption of data for secure transmission - this happens at Layer 6.
- Layer 5 - Session: When two devices, computers or servers need to “speak” with one another, a session needs to be created. Functions involve setup, coordination (how long should a system wait for a response, for example) and termination between the applications at each end of the session.
- Layer 4 – Transport: The Transport Layer deals with the coordination of the data transfer between end systems and hosts. How much data to send, at what rate, where it goes, etc. TCP and UDP port numbers work at Layer 4, while IP addresses work at Layer 3, the Network Layer.
- Layer 3 - Network: Most of the router functionality is found here. This layer is responsible for packet forwarding, including routing through different routers. IP addresses work here.
- Layer 2 – Data Link: Provides node-to-node data transfer (between two directly connected nodes), and also handles error correction from the physical layer.
- Layer 1 - Physical: Represents the electrical and physical representation of the system. Can include everything from the cable type, radio frequency link (as in an 802.11 wireless systems), as well as the layout of pins, voltages and other physical requirements.