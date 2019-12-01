## List of some useful Networking commands

##### 1. IP Addr

 To get the depth information of your network interfaces like IP Address, MAC Address information, use the following command as shown below. https://www.tecmint.com/ip-command-examples/

    ip addr show
    ip route show


##### 2. netcat
 `netcat` or `nc` is a handy command to verify the connectivity to an ip or website from a client terminal

        $ nc -zv www.google.com 443
          Connection to www.google.com 443 port [tcp/https] succeeded!


- all `nc` does not know anything about forming a HTTP request. All `netcat (nc)` does is connect to a server's port and send a string over it. To the server the request appears like a HTTP request and it sends a HTTP response.

- `lsof` is a utility that open files, including network sockets (listening or connected). Use `sudo lsof -i` to listen only network sockets



##### 3. Dig (domain information groper):
`dig` is a flexible tool for interrogating DNS name servers. It performs DNS lookups and displays the answers that are returned from the name server(s) that were queried. Most DNS administrators use dig to troubleshoot DNS problems because of its flexibility, ease of use and clarity of output. Other lookup tools tend to have less functionality than dig.


##### 4. tcpdump:
`tcpdump`  prints out a description of the contents of packets on a network interface that match the boolean expression; the description is preceded by a time stamp printed, by default, as hours, minutes, seconds, and fractions of a second since midnight.

    example: to check network traffic from your host to some remote host. In terminal one session type the below command:
    
    sudo tcpdump -n host 8.8.8.8

    In a second terminal session, run a ping to some network packet flowing in the first terminal one session:

    ping -c 3 8.8.8.8


##### 5. traceroute:
`traceroute`  tracks  the  route  packets  taken from an IP network on their way to a given host. It utilizes the IP protocol's time to live (TTL) field and attempts to elicit an ICMP TIME_EXCEEDED response from each gateway along the path to the host.

    example:
    traceroute www.google.com


##### 6. mtr:
`mtr` combines the functionality of the traceroute and ping programs in a single network diagnostic tool.

As  mtr  starts,  it  investigates  the network connection between the host mtr runs on and HOSTNAME by sending packets with purposely low TTLs. It continues to send packets with low TTL, noting the response time of the intervening routers.  This allows mtr to print the response percentage and response times of the internet  route to HOSTNAME.  

A sudden increase in packet loss or response time is often an indication of a bad (or simply overloaded) link. 

The results are usually reported as round-trip-response times in miliseconds and the percentage of packetloss.




