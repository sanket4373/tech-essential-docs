- HTTP is an application layer protocol over TCP which is a transport layer protocol, which in turn is over IP.
- A connection must be established between the client and server before they can communicate with each other, and HTTP uses the reliable TCP transport protocol to make this connection.
- By default, web traffic uses TCP port 80. 
- A TCP stream is broken into IP packets, and it ensures that those packets always arrive in the correct order without fail. 


#### Client-side Connection Handling

- On a client, an HTTP application is identified by a <IP, port> tuple. Establishing a connection between two endpoints is a multi-step process and involves the following:

1. resolve IP address from host name via DNS
2. establish a connection with the server
3. send a request
4. wait for a response
5. close connection


#### Server-side Connection Handling

The server mostly listens for incoming connections and processes them when it receives a request. The operations involve:

1. establishing a socket to start listening on port 80 (or some other port)
2. receiving the request and parsing the message
3. processing the response
4. setting response headers
5. sending the response to the client
6. close the connection if a Connection: close request header was found



