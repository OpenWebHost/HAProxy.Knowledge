https://www.haproxy.com/documentation/haproxy-configuration-manual/latest/#1.1

>By default HAProxy operates in keep-alive mode with regards to persistent connections: for each connection it processes each request and response, and leaves the connection idle on both sides between the end of a response and the start of a new request. When it receives HTTP/2 connections from a client, it processes all the requests in parallel and leaves the connection idling, waiting for new requests, just as if it was a keep-alive HTTP connection.
>
>HAProxy essentially supports 3 connection modes :
>  - keep alive    : all requests and responses are processed, and the client facing and server facing connections are kept alive for new requests. This is the default and suits the modern web and modern protocols (HTTP/2 and HTTP/3).
>
>  - server close  : the server-facing connection is closed after the response.
>
>  - close         : the connection is actively closed after end of response on both sides.
>
>In addition to this, by default, the server-facing connection is reusable by any request from any client, as mandated by the HTTP protocol specification, so any information pertaining to a specific client has to be passed along with each request if needed (e.g. client's source adress etc). When HTTP/2 is used with a server, by default HAProxy will dedicate this connection to the same client to avoid the risk of head of line blocking between clients.
