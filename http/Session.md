# Session

> `Session` is an authentication method that allows users to get access the data sent from the server.

> `HTTP` is stateless connection protocol

> The data is typically stored in server memory and looked upon each request via `session id`.

## How it works

* The user’s browser send the first request to the server.
* The server checks whether the browser has passed along the browser cookie that contained session information.
* If the server does not ‘know’ the client The server creates a new unique identifier `Session Id` and puts it in a Map (roughly), as a key, whose value is the newly created Session. It also sends a cookie response containing the unique identifier. The browser stores the session cookie containing the unique identifier and uses it for each subsequent request to identify itself uniquely with web server.
* If the server already knows the client – the server obtains the session data corresponding to the passed unique identifier found in the session cookie and serves the requested page.


