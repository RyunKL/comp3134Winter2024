# Week 2
## Objectives
Use information gathering techniques to perform network audits and discover network insecurities<br>
Recall security fundamental terms and diagrams & apply them to classify network discover and security auditing techniques

## Identifying a Server
**IP Address Look-Up**
If you know a name of an existing domain name, you can use online services to get information about its domain-name registration<br>
**STEPS**
1. Perform a search engine Search with the keyword "whois"
2. Navigate to any online service site
3. Perform lookups for 5 distinct domains (not sub-domains)
4. Create a text file named whois.txt and paste the data returned for all 5 queries

**Domain Name Look-Up**
If you would like to get an IP address of a specific host, you can use online services to accomplish this task<br>
1. Perform a search engine Search with the keyword "get ip of domain"
2. Navigate to any online service site
3. Perform lookups for 5 distinct domains (cannot include domains from above)
4. Create a text file named ipinfo.txt and paste the IP Address and Geolocation data returned for all 5 queries

## Ensure Server is Running
Ping is a computer network administration software utility used to test the reachability of a host on an Internet Protocol network.<br>

**Any Host Server Test**
1. Login into your Droplet server using ssh and GitBash
2. Open GitBash
3. Type in the following command
```
ssh root@IP_ADDRESS
```
When prompted, enter your droplet password (not needed if using SSH keys) Once you have successfully connected to your Droplet, install updates and apache2 utilities
```
apt-get update
apt-get install apache2-utils
```
Use the ping tool to determine if a server is up and running
```
ping <hostname>
```
For hostname use an IP address or any fully qualified domain name<br>
To ping for a specified time use this command
```
ping <hostname> -w <time_in_seconds>
```
## Path to Destination
Traceroute is command to displaying the route and measuring transit delays of packets across an Internet Protocol Network<br>

Use it to determine how you get form your host to destination host<br>
**Install Traceroute(On Remote Host)**<br>
To install traceroute on your droplet, type the following command
```
apt-get install traceroute
```
For windows machines you can use the traceroute command by typing this on the terminal, command prompt, or GitBash
```
tracert <hostname>
```
For Linux use this command
```
traceroute <hostname>
```

## NMAP
Nmap is a powerful network discovery and security auditing utility that is free, open-source, and easy to install. Nmap scans for vulnerabilities on your network, performs inventory checks, and monitors host or service uptime, alongside many other useful features.<br>

**Installation of nmap**<br>
Open GitBash window that is connected to your droplet via ssh<br>
To install name, execute the following steps
1) Install Nmap
2) Verify Nmap is installed
```
apt-get install nmap
nmap --version
```
**Using Nmap**<br>

To use Nmap to scan 1000 TCP ports, type the following command. Use various host names.
```
nmap {host_name}
```
To scan a single Port
```
nmap -p {port_number} {host_name}
```
To scan a range of ports
```
nmap -p {start_port_range}-{end_port_range} {host_name}
```
To scan 100 most common ports (Fast)
```
nmap-F <hostname>
```