# Firewall Basics using iptables

## Objective
- Create simple iptables rules.
- Allow and deny specific ports.
- Demonstrate blocking a port scan using Nmap.

## Commands Used

iptables --version

sudo iptables -L -n -v
sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT

sudo iptables -A INPUT -p tcp --dport 80 -j DROP
nmap -p 80 <Target-IP>

sudo iptables -D INPUT -p tcp --dport 80 -j DROP

## Result
Successfully created firewall rules and verified that Nmap reports port 80 as **filtered**, demonstrating that the firewall blocked the port scan.

commands.txt
iptables --version
sudo iptables -L -n -v
sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT
sudo iptables -A INPUT -p tcp --dport 80 -j DROP
nmap -p 80 <Target-IP>
sudo iptables -D INPUT -p tcp --dport 80 -j DROP
