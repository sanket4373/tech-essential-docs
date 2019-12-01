### What is a Domain Name System?

According to this [article](https://www.digitalocean.com/community/tutorials/an-introduction-to-dns-terminology-components-and-concepts), The domain name system, more commonly known as “DNS” is the networking system in place that allows us to resolve human-friendly names to unique addresses.

In short, DNS tranlates a hostname into an IP address for that host.

#### A-Record:
It is used to find the address of a computer connected to the internet from a name (domain name). In other words, The "A” record is used to map a host to an IPv4 IP address

`Domain Name ---> Registrar ---> IP Address`

- If DNS goes down your site can't be reached by users.

- DNS records expires
- DNS is part of the security mechanism for HTTP which includes SSL encryption and cookie privacy

- DNS record have a TTL (Time to Live) which tells the caches on how long to cache them for

#### The Resolver:
The DNS client code is built into every OS.


#### C-Name or FQDN:
It is used to specify that a domain name is an alias for another domain. 
example `www.github.com` is an c-name or alias for `github.com`


#### Search Domain:
A setting in the resolver configuration that makes the resolver look up names inside a domain

example of DNS worker in action: 

- `A` record for `www.google.com` can be found on the `name server` for `www.google.com`.
- `NS` record for `www.google.com` resides in the `com` server which is a `gTLD (Global Top level Domain)
- The `NS` for `.com` are stored in the root servers 







