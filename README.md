# Session Based Authentication Learning Project

Lets take a step back and know about *HTTP Protocol* and how it works. HTTP is a stateless protocol, which means that each request from a client to server is treated as an independent transaction that is unrelated to any previous request. This means that the server does not retain any information about the client between requests.

*Sessions* allow us to change that. With sessions, the server has a way to associate some information with the client so that when the same client requests the server, it can retrieve that information.

## So, what is this session based authentication?

Session based authentication is a stateful authentication technique where we use sessions to keep track of the authenticated user. Here is how it works:

- User submits the login request for authentication.

- Server validates the credentials. If the credentials are valid, the server initiates a session and stores some information about the client. This information can be stored in memory, file system, or database. The server also generates a unique identifier that it can later use to retrieve this session information from the storage. Server sends this unique session identifier to the client.

- Client saves the session id in a cookie and this cookie is sent to the server in each request made after the authentication.

- Server, upon receiving a request, checks if the session id is present in the request and uses this session id to get information about the client.


*I have intentionally kept the project strictly relevant to the Session Based Authentication and have left out a lot of details that a production-ready application may require.*
