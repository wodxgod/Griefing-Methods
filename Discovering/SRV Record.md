# SRV Record

**Overview**

SRV Record (Service Record) is an internet protocol used to among other retrieve the host address and port for a specific service through DNS (Domain Name System). In some cases, it can be very efficient to use as a server discovery method.

A typical SRV record has the following format: `_<service>._<transport protocol>.<domain>`.

Example: `_minecraft._tcp.example.com`.

Using the ping command doesn't always return the correct IP-address of the server due to different hosts hosted on the same domain, CDN systems and other services that protects the servers IP-address.
> Related: [Domain to IP](https://github.com/wodxgod/Griefing-Methods/blob/master/Discovering/Domain%20to%20IP.md)

Using the following Python code will send a DNS query to the specified server and return the IP-address and port for the Minecraft server hosted on that domain:
```python
import dns.resolver
import socket

def lookup(addr):
    host = addr
    port = None
    if ':' in addr:
        x = addr.split(':')
        if len(x) > 2:
            raise ValueError(f'Invalid address: \'{addr}\'')
        host = x[0]
        port = int(x[1])
    if not port:
        port = 25565
        try:
            answers = dns.resolver.query('_minecraft._tcp.' + host, 'SRV')
            if len(answers):
                answer = answers[0]
                host = str(answer.target).rstrip('.')
                port = int(answer.port)
        except Exception:
            pass
    return (host, socket.gethostbyname(host), port)

print(lookup(input('Server: ')))
```
