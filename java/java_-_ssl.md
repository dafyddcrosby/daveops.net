# Java - SSL
Debugging
---------



  # print each handshake message
  java -Djavax.net.debug=ssl:handshake MyApp

AES intrinsics
--------------

Requires Java 8 and Intel 2010+ Westmere



  -XX:+UseAES -XX:+UseAESIntrinsics

Links
-----


* <https://docs.oracle.com/javase/7/docs/technotes/guides/security/jsse/ReadDebug.html>
* <https://docs.oracle.com/javase/7/docs/technotes/guides/security/jsse/JSSERefGuide.html#Debug>


