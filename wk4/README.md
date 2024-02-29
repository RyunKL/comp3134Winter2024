# Week 4
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

_Installation of Iptables_<br>
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
Create a text file named **iptables_rules_1.txt** and copy all of the output of the command above<br><br>

_Manual for iptables_<br>
A manual of command lists and describes all of its options
[ip table commands](https://linux.die.net/man/8/iptables)<br><br>

_Using iptables_<br>
A valid iptables command takes the following syntax:
```
iptables -A <chain> -i <interface> -p <protocol (tcp/udp)>
-s <source> --dport <port no.> -j <target>
```
## Getting Started with WireShark

_What is WireShark?_<br>
Wireshark is a free and open-source packet analyzer. It is used for network troubeshooting analysis, software and communications protocol development, and education.<br><br>

_How does WireShark work?_<br><br>
Whireshark is a packet sniffer and analysis tool that captures network traffic on the local network and stores that data for offline analysis. Wireshark captures network traffic from Ethernet, Bluetooth, Wireless, Token, Ring, Frame Relay connection, and more.<br><br>
**NOTE** A packet is a single message from any network protocol<br><br>

_Installation_<br><br>
If you are using WireShark on your personal machines, please following the installation instructions below.<br><br>

[Official WireShark Download Website](https://www.wireshark.org/download.html)

## Runningg WireShark for the First Time

Louching WireShark for the first time, you will see a welcome screen. If you do not see this or you want to start a new capture click on Capture -> Options from the menu-> Select either Ethernet or Wi-fi<br><br>

_Display Filter_<br><br>
There may be times where you would like tto capture all traffic but filter the captured traffic. To accomplish this, navigate to the **Filter Toolbar**. For more, Here is a guide to futher understand how to best use the filter toolbar

[Filter Toolbar Guide](https://wiki.wireshark.org/DisplayFilters#Examples)<br><br>

_Capture Filters_<br>
There may be times where you'd like to only capture specific traffic. To accomplish this, start a new capture by clicking on Capture -> Options from the Menu. Here is a guide

[Capture Filters Guide](https://wiki.wireshark.org/CaptureFilters#Capture_filter_is_not_a_display_filter)<br><br>

_Switch Captures_<br>
Stop the current Capture by clicking on Capture -> Stop, Start a new Capture by clicking on Capture ->Start<br>

Select another Capture Input Interface<br>
Start the new capture<br>

## Using WireShark
Execute the following steps using WireShark. For each step, take a screenshot named **using_wireshark_N.png** where N represents the step number.
1. Filter only show ARP or DNS packet traffic
2. Filter to only show UDP or TCP packet traffic
3. Filter to show TCP packet traffic on any port greater than 3000
4. Filter to only show HTTP packet traffic
5. Filter to how only HTTP post method request packet traffic(use a web page form so you can see at least one entry)
6. Filter to show UDP packet traffic that contain the string "google"
7. Filter to show HTTP packett traffic where the page was not found
8. Filter to show TCP packet traffic where the acknowledgement flag was set
9. Select any two IP addresses and show the Flow Graph demonstrating a 3-way handshake between the two IP addresses

## Install and Use tcpdump
TCPdump is a command line packet sniffer<br><br>

_Installation_<br>
Tcpdump may already come installed in your Linux distribution. In case not, to install tcpdump, type the following command
```
apt-get install tcpdump
```
<br>

_UsingTcpdump_<br>
The following link provides a guide on how to use tcpdump. Create text files that show the command and result of each step with the filename format of **tcpdump_step_N.txt** where N represents the step number.

[tcp dump Guide](https://www.tecmint.com/12-tcpdump-commands-a-network-sniffer-tool/)
