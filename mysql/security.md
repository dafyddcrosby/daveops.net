# security
@MySQL

Don't place DB on same instance as application
----------------------------------------------

If the application is vulnerable to a file disclosure attack, it could allow attacker to download the DB files directly. This can be mitigated by proper file permissions, but a locked down ACL on a networked MySQL server is just as good (and makes the application more scalable as well).

