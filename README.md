# Experimental DNS server to act as a `proxy_pass` `resolver` for nginx to bounce your requests to depending on SQLite lookup data

Experimental Python based DNS server that lets you use SQLite as a nginx proxy_pass `resolver` that performs an SQLite query to decide where to proxy_pass the request to.

( Asks a SQLite DB what the real IP for a lookup should be and returns that so `proxy_pass` can use it )

Based on https://github.com/paulc/dnslib/blob/master/dnslib/fixedresolver.py


`docker-compose up`

Then

- http://127.0.0.1/google Lookup "google" in the SQLite then resolve to an IP that hopefully still works and proxy_pass you there
- http://127.0.0.1/test-container Fallback example, key doesnt exist so we fallback to using the existing defined docker hosts/containers

### See
- http://nginx.org/en/docs/http/ngx_http_core_module.html#resolver

### Note

Use at own risk, may or may not scale, may or may not rename your dog and set your house on fire.
