# An experimental DNS server to act as a `resolver` for nginx to bounce your requests to depending on the SQLite lookup data

Experimental Python DNS server that lets you use SQLite as a nginx proxy_pass `resolver` that performs an SQLite query to decide where to proxy_pass the request to.
