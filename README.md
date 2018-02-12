[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)

ansible-role-certbot
====================

Will just generate letsencrypt.org certificates using certbot and webroot on debian-based systems.

Vars
----

	certbot__email: test@nosuchdomain.xyz

	# map of cert name => map webroot => lsit of names
	# for each maincertname a cert will be generated using the webroot map => domainname as names
	certbot__certs:
	  dom1.tld1:
	    /srv/www/dom1:
	      - dom1.tld1
	      - a.dom1.tld1
	      - b.dom1.tld1
	      - a.dom2.tld2
	    /srv/www/dom3
	      - dom3.tld3
	  dom2.tld2:
	    /srv/www/dom2
	      - dom2.tld2

