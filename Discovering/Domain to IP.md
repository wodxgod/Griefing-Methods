# Domain to IP

In some cases you need the servers IP-address, but you only have it's domain e.g. `example.com`. There are many different ways to retrieve the servers IP-address from its domain.

One way of getting the IP-address by its domain, is by using the default shell command `ping`. Using the command `ping <domain>` will return the servers IP-address.

Example of the output from the ping command using the domain `example.com`.
```
$ ping example.com

Pinging example.com [93.184.216.34] with 32 bytes of data:
Reply from 93.184.216.34: bytes=32 time=95ms TTL=55
Reply from 93.184.216.34: bytes=32 time=92ms TTL=55
Reply from 93.184.216.34: bytes=32 time=93ms TTL=55
Reply from 93.184.216.34: bytes=32 time=93ms TTL=55

Ping statistics for 93.184.216.34:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 92ms, Maximum = 95ms, Average = 93ms

$
```

In the square brackets you can see the servers IP-address.
> Read about how to bypass IP protection at: [SRV Records](https://github.com/wodxgod/Griefing-Methods/blob/master/Discovering/SRV%20Records.md)