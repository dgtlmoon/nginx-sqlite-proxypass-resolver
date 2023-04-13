# An experimental DNS server to act as a `resolver` for nginx to bounce your requests to depending on the SQLite lookup data

Experimental Python DNS server that lets you use SQLite as a nginx proxy_pass `resolver` that performs an SQLite query to decide where to proxy_pass the request to.


`docker-compose up`

Then

- http://127.0.0.1/google Lookup "google" in the SQLite then resolve to an IP that hopefully still works and proxy_pass you there
- http://127.0.0.1/test-container Fallback example, key doesnt exist so we fallback to using the existing defined docker hosts/containers

