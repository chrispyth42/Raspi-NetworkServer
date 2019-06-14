# Raspi-NetworkServer
A repository of documentation files, containing steps that I took to make a raspberry pi be a server to manage a small network. Running on command line only, raspbian (debian) linux. These files serving as a manual in case I need to make changes to the settings, or need to repeat the process later on

### Apache-PHP.txt
A brief list of commands on how to install and test Apache2 and PHP

### DHCP.txt
An installation guide for the package 'isc-dhcp-server', and how to configure it to distribute IPs over the eth0 interface for the 10.0.0.0/16 IP range

### DNS.txt
An installation and setup guide for the DNS server package 'bind9'. On my network topology which consists of an ethernet 10.0.0.0/16 network, and a wireless 192.168.1.0/24 network. Also outlining how to manually create local domains and assign domain names to end devices: giving 10.0.0.0 the 'chris.local' suffix, and 192.168.1.0 the 'home.local' suffix

### SQL.txt
A guide on how to install the popular database package 'mysql-server', including instructions on how to create a database and grant priveleged access, as well as how to get the server online

### Samba.txt
Instructions on what package is needed to give the PI ntfs file system support (in order to successfully mount and use an external NTFS hard drive), and how to install the Samba fileshare server and configure it to share a directory on the network.  
