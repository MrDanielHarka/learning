# The Internet


## Notes

21.03.28.

### The Internet Layers

- HTTP & DNS: Manage the sending and receiving of web files.
- TCP/IP & Routing: Break down and transport packets.
- Wires, cables & Wifi: Binary sequences of 1's & O's are sent physically.

### HTTP (Hypertext Transfer Protocol)

- Allows communication between hosts and clients.
- Supports a mixture of network configurations.
- Communicating on request/response pair.

### The URL (Uniform Resource Locator) ###

- The way of sending request messages.
- Components:
    - Protocol: Typically http or https.
    - Port: Default is 80, but can be set explicitly.
    - Local path: Resource on the server.

### Verbs ###

- "The action that should be performed on the host is specified via HTTP verbs.""
- Most common request verbs:
    - GET: fetch an existing resource. URL contains all necessary info the server needs to locate and return the resource.
    - POST: create a new resource. Usually carryies payload that specifies the data for the new resource.
    - PUT: update an existing resource. Payload may contain the updated data for the resource.
    - DELETE: delete an existing resource.
- Less commong verbs that HTTP also supports:
    - HEAD: this is similar to GET, but without the message body. It's used to retrieve the server headers for a particular resource, generally to check if the resource has changed, via timestamps.
    - TRACE: used to retrieve the hops that a request takes to round trip from the server. Each intermediate proxy or gateway would inject its IP or DNS name into the Via header field. This can be used for diagnostic purposes.
    - OPTIONS: used to retrieve the server capabilities. On the client-side, it can be used to modify the request based on what the server can support.

### Status Codes ###

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

**4xx: Client Error**

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

**5xx: Server Error**

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