Private VPN on Public Cloud (Azure/AWS/GCP/DigitalOcean etc)

The Problem: When trying to access gaming servers like CS:GO/R6S on university LAN networks, the routing is incredibly poor.

- Sometimes there is packet loss upto 50 percent
- Very high ping or round trip latency times
- Server disconnection issues

The typical latency to various nearby servers looks like this:

- Mumbai: 24ms
- Chennai: 39ms
- Singapore: 65ms
- Dubai: 75ms

However, when playing on university LAN connection, the numbers were 400ms. When I identified the server IP address and did a traceroute, I found that the in-game UDP traffic was being routed from India through USA and then to some server.

But this was not the case for non-game TCP traffic. So I decided to create to deploy private VPN serves on various public cloud nodes which fixed the problem to a large extent.

- Packet Loss dropped to <1ms
- Even though connection to VPN was TCP while in game traffic was UDP, there were little no server lag
- Ping dropped from 400ms to less than 120ms

---------------------------------------------------------------------------------------------------------------------

- To establish the VPN connection, first an account is needed at one of the public cloud service providers. For example, Microsoft Azure, Google Cloud Platform, Amazon Web Services etc

- After signing up, you need to select an appropriate availability zone and server location nearest to where your gaming server is located. 

- Create a Windows Virtual Machine on Login to it remotely

- Download & Install SoftEther VPN Server on the cloud VM
http://www.softether-download.com/en.aspx?product=softether

- Download Softether VPN client and install on PC
http://www.softether-download.com/en.aspx?product=softether

- 

- 

- 

- 
