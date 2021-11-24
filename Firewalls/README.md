Explanation of the Iptables Rules

Strat Script by typing vi script name. Type #!/bin/bash. Then start the iptables rules. After finishing press ESC and: wq to save and exit. 
Make the script executable by running the chmod +x and the script path.

sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT.  
The first command is to allow incoming traffic from port 80. 
The rule starts with -A which tells iptables to add a rule. 
INPUT means that the rules for the input chain.
 -p to indicate the protocol for the rule. 
-tcp is the rule protocol. 
–dport means the destination port.
 80 is the port number.
 -j is to indicate what should happen. 
Accept to allow the connection.

sudo iptables -A INPUT -p tcp --dport 8080 -j ACCEPT.  
This command allows traffic from port 8080. 
-A tells iptables to add a rule
INPUT means that the rules for the input chain.
-p to indicate the protocol for the rule. 
-tcp is the rule protocol. 
– dport is the destination port.
 8080 is the port number.
-j is to indicate what should happen. 
Accept to allow a connection.

sudo iptables -t nat -I PREROUTING -p tcp --dport 80 -j REDIRECT --to-port 8080. 
This rule to forward traffic from port 80 to port 8080.
The rule starts with -t nat which means the rule uses the NAT packet matching table.
-I PREROUTING to alternate incoming traffic.
-p to indicate the protocol for the rule. 
-tcp is the rule protocol. 
–dport is the destination port.
 The 80 is the port.
-j is to indicate what should happen. 
REDIRECT to send the traffic to different destination. 
--to-port to indicate the port that traffic must redirect to.

sudo iptables -A INPUT -p tcp --destination-port 3306 -j ACCEPT. 
This command will allow remote access from all IP addresses on the internet through the MYSQL port.
-A tells iptables to add a rule.
INPUT means that the rules for the input chain.
-p to indicate the protocol for the rule. 
-tcp is the rule protocol. 
–dport is the destination port.
--destination-port is to indicate the destination port.
3306 is MYSQL port.
-j is to indicate what should happen. 
Accept to allow connection.

sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT.  
This command to allow all incoming SSH connections.
-A tells iptables to add a rule.
INPUT means that the rules for the input chain.
-p to indicate the protocol for the rule. 
-tcp is the rule protocol –dport is the destination port.
-j is to indicate what should happen. 
Accept to allow connection.

sudo iptables -A OUTPUT -p tcp --sport 22 -j ACCEPT. 
 This command allows all outgoing SSH connection.
  -A tells iptables to add a rule.
OUTPUT means that the rules for the output chain.
-p to indicate the protocol for the rule. 
-tcp is the rule protocol.
–dport is the destination port
22 is the port for SSH traffic.
-j is to indicate what should happen. 
Accept to allow connection.

sudo iptables -A OUTPUT -p tcp --dport 25 -j REJECT. 
This command to reject all outgoing SMTP mail.
  -A tells iptables to add a rule.
OUTPUT means that the rules for the output chain.
-p to indicate the protocol for the rule. 
-tcp is the rule protocol.
 –dport is the destination port.
25 is the port for SMTP traffic.
-j is to indicate what should happen.
REJECT to reject outgoing traffic to port 25 connection.


sudo iptables -A INPUT -p tcp --dport 110 -j ACCEPT. 
 This command to allow is to allow a server to respond to POP connections.
 -A which tells iptables to add a rule. 
 INPUT means that the rules for the input chain.
-p to indicate the protocol for the rule. 
-tcp is the rule protocol.
–dport is the destination port.
 The 110 is the port.
 -j is to indicate what should happen. 
Accept to allow a connection.


sudo iptables -A OUTPUT -p tcp --sport 110 -j ACCEPT. 
   This command to allow outgoing POP3 connection.
    -A which tells iptables to add a rule. 
    OUTPUT means that the rules for the input chain.
   -p to indicate the protocol for the rule. 
   -tcp is the rule protocol.
   –sport is the source port.
    The 110 is the port.
   -j is to indicate what should happen. 
   Accept to allow a connection.


sudo iptables -A INPUT -m mac --mac-source 00:0F:EA:91:04:08 -j DROP. 
  This to drop all connections coming from a specific MAC address.
  -A which tells iptables to add a rule. 
  INPUT means that the rules for the input chain.
 -m mac to indicate the mac address for the rule. 
 -j is to indicate what should happen.
 Drop to drop the connection.

sudo iptables -A INPUT -p tcp --dport 22 -m mac --mac-source 00:0F:EA:91:04:08 -j ACCEPT. 
This command allows SSH access to specific MAC.
-A which tells iptables to add a rule. 
INPUT means that the rules for the input chain.
-p to indicate the protocol for the rule. 
-tcp is the rule protocol.
–dport means the destination port.
-m mac to indicate the mac address for the rule. 
-j is to indicate what should happen.
Accept to allow connection.


sudo iptables -A INPUT -p icmp --icmp-type echo-request -j REJECT. 
This command to block pings.
-A which tells iptables to add a rule. 
INPUT means that the rules for the input chain.
-p to indicate the protocol for the rule. 
icmp --icmp-type echo-request means ping requests.
-j is to indicate what should happen.
REJECT to reject a connection.



sudo iptables -A INPUT -p tcp --dport 22 -j DROP. 
 This command to drop all incoming SSH traffic
-A tells iptables to add a rule.
INPUT means that the rules for the input chain.
-p to indicate the protocol for the rule. 
-tcp is the rule protocol –dport is the destination port.
-j is to indicate what should happen. 
DROP to drop all connection.

sudo iptables -A OUTPUT -p tcp --sport 22 -j Drop. 
 This command to drop all outgoing SSH traffic.
-A tells iptables to add a rule.
OUTPUT means that the rules for the output chain.
-p to indicate the protocol for the rule. 
-tcp is the rule protocol –dport is the destination port.
-j is to indicate what should happen. 
DROP to drop all connection.


Iptables can be used to prevent DDOS attacks by setting iptables rules, which can be by running a rule or writing a script. Some of these rules are blocking invalid packets,
blocking new packets that are not SYN, blocking uncommon MSS values, blocking packets with bogus TCP flags, and blocking spoofing packets that have private subnets.

