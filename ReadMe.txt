
Sometimes Cocoa developers need an HTTP server in their code. Perhaps they're writing a file-sharing app, or maybe they want to allow website links to communicate with built-in software similar to iTMS links. Obviously the built-in apache server is not an option. Thus the need for a small, lightweight, embedded HTTP server. This is what we needed for Mojo and we found a few available solutions:
	•	Apple's CocoaHTTPServer
	•	CultureCode's Simple HTTP Server
	•	WuffHTTPD for $100 USD

We liked Apple's the best because it was free and was built using standard networking sockets and streams. However, it didn't have everything we needed, and it seemed to have a few memory leaks. (We patched a few, but it still looked like it was leaking somewhere...) So with Apple's framework for an HTTP server tucked under our arm we set out to make our own. We wanted the following:
	•	Built in support for bonjour broadcasting
	•	IPv4 and IPv6 support
	•	Asynchronous networking using standard Cocoa sockets/streams
	•	Digest access authentication
	•	TLS encryption support
	•	Extremely FAST and memory efficient
	•	Heavily commented code
	•	Very easily extensible

This is the result of our hard work.

http://code.google.com/p/cocoahttpserver/