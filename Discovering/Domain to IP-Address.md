# Domain to IP-Address

In some cases you need the servers IP-address, but you only have it's domain e.g. `example.com`. There are many different ways to retrieve the servers IPv4 address from it's domain.

One way of getting the IP-address by it's domain, is by using the default command line command `ping`. Using the command `ping <domain>` will return the server's IPv4 address.

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
> Read about how to bypass IP protection at: [IP Sniffing](https://github.com/WodxTV/Griefing-Methods/blob/master/Discovering/IP%20Sniffing.md) and [SRV Records](https://github.com/WodxTV/Griefing-Methods/blob/master/Discovering/SRV%20Records.md)