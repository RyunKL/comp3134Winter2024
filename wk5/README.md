# Week 5
## Objective
Tracing network communication and analyze network activity in effort to identify and filter various protocols and network ports before and after implement various tactics to attack a network or application

## Packet Sender
_What is Packet Sender_<br>
packet Sender is an open source utility to allow sending and receiving TCP, UDP, and SSL (encrypted TCP) packets. The mainline branch officially supports Windows, Mac, and Desktop Linux(with Qt). Other places may recompile and redistribute Packet Sender. Packet Sender is free and licensed GPL v2 or later. It can be used for both commercial and personal use.<br>

_Packet Sender Uses_<br>
* Controlling network-based devices in ways beyond their original apps
* Test automation (using its command line tool and/or hotkeys)
* Testing network APIs (using the built in TCP, UDP, SSL clients)
* Malware analysis (using the built in TCP, UDP, TCP, SSL servers)
* Troubleshooting secure connections (using SSL )
* Testing network connectivity/firewalls (by having 2 packet senders talk to each other)
* Stress-testing a device (using intense network generator tool)
* Tech support (by sending customers a portable packet sender with pre-defined settings and packets)
* Sharing/saving/collaboration using the packet sender cloud service.

## Getting started with Packet Sender
When you launch Packet sender you will be presented with the following screen<br>

_Panels_<br>

1. This area is where you create a packet
 a. You create the packet name and data in hex and ASCII
 b. You input the desntiation delay and protocol of the packet
 c. Click "Send" to immediatly send. Click "Save" to send later.

2. Is the area of your saved packets
 a. Clicking on the send button will send or resend the packet
  i. Durring packet resending there will be a button to cancel
 b. You can double-click tot directly edit fields in this table
 c. Select multiple by holding down the shift button and selecting multiple packets. The click "Multi-send" in Panel 1 area.
3. Is the log of packet traffic

_Other Notable Areas/Notes_<br>
* In the bottom right, there are UDP, TCP and SSL server status and ports. You can click to activate or deactivate these. Packet Sender supports binding to any number of ports.
* Durring packet resending, there will be a button to cancel all resends
* Fields can be rearranged by going to file -> settings then going to the Display tab
* Please check your firewall. Windows aggressivly blocks TCP-based servers. Packet Sender will still work if t he firewall blocks it, but it can't receieve unsolicited TCP-based packets

_Hotkeys/Keyboard Shortcuts_<br>

The fields at the top can be navigated using CTRL+1, CTRL+2, etc up to CTRL+8 (send button) On mac the shortcut key is Command<br>

_Logging and Saving_<br>
T osave the log of your Packet Traffic area, clickc on the "save log" button. To save a selected packet, select the packet and click "save traffic packet". To copy the ASCII data of a packet, select the packet and click "copy to clipboard".<br>

_Intense Traffic Generator_<br>




