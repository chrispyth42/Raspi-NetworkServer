# Raspi-NetworkServer
A repository of documentation files, containing steps that I took to configure a raspberry pi to operate as a network server. (running on Raspbian linux). These files serve as a manual in case I need to make changes to the settings, or need to repeat the process later on. This device is configured with the IP address: 192.168.42.2 on Ethernet, and 192.168.1.4 on Wlan 

### Installed Services
    DHCP Server
    DNS Server
    Samba Fileshare
    Mysql Server
    Apache Webserver

### DHCP
Is delivered via the package 'isc-dhcp-server'. It's configured to distribute IP addresses on the 192.168.42.0/24 subnet. It configures hosts on that range to use itself as the DNS server, and supplies them DNS suffix 'chris.local'

### DNS
Is delivered via the package 'bind9'. It has 192.168.1.1 (my home router), and 8.8.8.8 (google) specified as the domain name servers to reference when it recieves a request it doens't have stored. Having a local DNS server like this allows for marginally better internet browsing speeds (DNS being cached 2 feet away from my desktop), and allows for the manual entry of 'A' records; granting devices on LAN domain names

### Samba Server
This package makes it incredibly straightforward to bounce files between my windows desktop, and linux raspberry pi. The directory it's running is a share is on an external hard drive; serving as an excellent network attached storage

### Apache/Mysql
These servers, for the most part, work out of the box just fine. The stored documentation I have on them specifies which commands to run to install php along with apache, as well as how to create and grant permission to accounts in MySQL
