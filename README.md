# HTTP2 :: The Fast Web


Google's SPDY protocol become the basis for HTTP2, the next version on HTTP.

## Future of Internet

1. Multiplexing feature that can deliver more HTTP requests at once so H2 can load website/webapps faster than ever.

2. A larger number of requests is no longer a problem - So problems with Spriting, inlining can be avoided.

3. Use Existing APIs - That means no need to change the existing application code, changing the protocal will work.

4. Cheaper Requestes
    a) Multiplexing and concurrency: Several requests can be sent in rapid succession on the same TCP connection, and responses can be received out of order - eliminating the need for multiple connections between the client and the server [“head-of-line blocking” Solved]

    b) Header compression: HTTP header size is drastically reduced

    c) Stream dependencies: the client can indicate to the server which of the resources are more important than the others

    d) Server push: The server can send resources the client has not yet requested

5. Security
    a) Not mandates HTTPS, but its good for privacy and user protection.
    b) The new protocol does not support things like SSL renegotiation, SSL compression, or any protocol before TLS 1.2 with weak ciphers. So on that level the protocol makes the web a lot safer.
    

    [HTTP/2 has four huge security vulnerabilities](https://betanews.com/2016/08/04/http-2-security-vulnerabilities/)
    [HTTP/2 Will Break Your Security – Here’s How to Fix it](https://blog.radware.com/security/2015/09/http2-security-fix/)
