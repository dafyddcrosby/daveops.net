# DNS
Reverse lookup
--------------

``dig -x [ip addr]``

Query name server for IP addresses
----------------------------------

``nslookup [name] [dns server]``

Get nameserver glue records
---------------------------

	# get root servers
	dig NS com
	# get glue records
	dig NS example.com @b.gtld-servers.net


Get SOA (serial, refresh, retry, expiry, minimum)
-------------------------------------------------

``dig +short example.com soa``

Add Route53 subdomain to zone file
----------------------------------
	; drop this in the example.com zone file
	$ORIGIN subdomain.example.com.
	@ IN NS ns-x.awsdns-x.net.
	@ IN NS ns-x.awsdns-x.com.
	@ IN NS ns-x.awsdns-x.co.uk.
	@ IN NS ns-x.awsdns-x.org.


Links
-----


* [Kaminsky DNS Vulnerability](http://www.unixwiz.net/techtips/iguide-kaminsky-dns-vuln.html)
* [Cricket Liu's DNS Advisor](http://ww2.infoblox.com/services/dns_advisor_tool.cfm)

