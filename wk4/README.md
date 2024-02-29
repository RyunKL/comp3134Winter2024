# Week 2
## Objectives
Demonstrate passive sniffing using WireShark in effort to identify & baseline network traffic using network monitoring tools

## Server Firewall
By default, there are many ports that are open of a typical Linux distribution default installation. A firewall is a system that provides network security by filtering incoming and outgoing network traffic based on a set of user-defined rules. The purpose of a firewall is  to reduce or eliminate the occurrence of unwanted network communications while allowing all legitimate communication to flow freely.

_IPtables_
Iptables is a firewall program for Linux that will monitor traffic from and to yoru server using tables. These tables contain sets of rules, called chains, that will filter incomingg and outgoing data packets. When a packet matches a rule, it is given a **target**, which can be another chain or one of these speccial values

> **ACCEPT**&nbsp;&nbsp;&nbsp;&nbsp;Will Allow the packet to pass through<br>
> **DROP**&nbsp;&nbsp;&nbsp;&nbsp;Will not let the packet pass through<br>
> **RETURN**&nbsp;&nbsp;&nbsp;&nbsp;Stops the packet from traversing through a chain and tell it to go back to the previous chain

The Three common chains are:

> **INPUT**&nbsp;&nbsp;&nbsp;&nbsp; Controls incoming packets to the server<br>
> **FORWARD**&nbsp;&nbsp;&nbsp;&nbsp; Filters incoming packets that will be forwarded somewhere else<br>
> **OUTPUT**&nbsp;&nbsp;&nbsp;&nbsp; Filters packets that are going out from your server

_Installation of Iptables_
Most Linux distributions should have iptables installed by default. To check run the following command
```
man iptables
```
If it is not installed, run the following commands
```
apt-get update
```
```
apt-get install iptables
```
View all defined rules of iptables
```
iptables -L -v
```


