# Python - HTTPServer
@Python


Basic HTTP server
-----------------

```python

 from BaseHTTPServer import HTTPServer, BaseHTTPRequestHandler
 from SocketServer import ThreadingMixIn
 
 class RedirectHandler(BaseHTTPRequestHandler):
 def do_HEAD(self):
 self.send_response(200)
 self.send_header("Content-type", "text/html")
 self.end_headers()
 
 def do_GET(self):
 self.send_response(200)
 self.send_header("Content-type", "text/html")
 self.end_headers()
 self.wfile.write("<html><head><title>Example</title></head>")
 self.wfile.write("<body>%s</body></html>" % self.path)
 
 class ThreadedHTTPServer(ThreadingMixIn, HTTPServer):
 """
 Thread the responses
 """
 if __name__ == '__main__':
 host = "0.0.0.0"
 port = 8080
 try:
 httpd = ThreadedHTTPServer((host, port), RedirectHandler)
 httpd.serve_forever()
 except:
 print "Could not bind to host %s port %i\n" % (host, port)
```
