# HTTP2 :: The Fast Web

### Expect 50% increased web performance


Google's SPDY protocol become the basis for HTTP2 - the next superfast HTTP Version.

## Future of Internet

1. Multiplexing feature that can deliver more HTTP requests at once so H2 can load website/webapps faster than ever.

2. A larger number of requests is no longer a problem - So problems with Spriting, inlining can be avoided.

3. Use Existing APIs - That means no need to change the existing application code, changing the protocal will work.

4. Cheaper Requestes

    a) Multiplexing and concurrency: Several requests can be sent in rapid succession on the same TCP connection, and responses can be received out of order - eliminating the need for multiple connections between the client and the server [“head-of-line blocking” Solved]

    b) Header compression: HTTP header size is drastically reduced

    c) Stream dependencies: the client can indicate to the server which of the resources are more important than the others

    d) Server push: The server can send resources the client has not yet requested

5. No More Text, it’s a binary protocol. 
    
    While binary protocols have lower overhead to parse, as well as a slightly lighter network footprint, the real reason for this big change is that binary protocols are simpler, and therefore less error-prone. So debugging will be an issue(check below).

6. Security

    a) TLS/HTTPS security by default

    b) Not mandates HTTPS, but its good for privacy and user protection.

    c) The new protocol does not support things like SSL renegotiation, SSL compression, or any protocol before TLS 1.2 with weak ciphers. So on that level the protocol makes the web a lot safer.
    
    ### Some important links to check for security:

    <a href="https://betanews.com/2016/08/04/http-2-security-vulnerabilities/" target="_blank">HTTP/2 has four huge security vulnerabilities</a>

    <a href="https://blog.radware.com/security/2015/09/http2-security-fix/" target="_blank">HTTP/2 Will Break Your Security – Here’s How to Fix it</a>


### Check Browser support: http://caniuse.com/#search=http2

## What to do to enable HTTP2?

Implementation Listing - (https://http2.github.io/)[https://http2.github.io/]

1. #### <a href="https://http2.akamai.com/" target="_blank">Akamai</a>: 

    Akamai customers can enable it right now with a few clicks without requiring any changes on the origin infrastructure.

2. #### <a href="https://www.iis.net/learn/get-started/whats-new-in-iis-10/http2-on-iis" target="_blank">IIS</a> :

    Windows 10 or Windows Server 2016 supports HTTP/2

3. #### <a href="https://geekflare.com/http2-implementation-apache-nginx/" target="_blank">Apache & Nginx</a>

4. <a href="https://support.cloudflare.com/hc/en-us/articles/115002816808-How-do-I-enable-HTTP-2-Server-Push-in-WordPress" target="_blank">How do I enable HTTP/2 Server Push in WordPress</a>

5. <a href="https://aws.amazon.com/blogs/aws/new-http2-support-for-cloudfront/" target="_blank">HTTP/2 Support for Amazon CloudFront</a>

6. <a href="https://kinsta.com/learn/what-is-http2/" target="_blank">What is HTTP2?</a>


#### How do I debug HTTP/2 if it’s encrypted? 

Use <a href="https://developer.mozilla.org/en-US/docs/Mozilla/Projects/NSS/Key_Log_Format" target="_blank">NSS keylogging</a> in combination with the Wireshark plugin (included in recent development releases). This works with both Firefox and Chrome.

