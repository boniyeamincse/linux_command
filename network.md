# Networking Commands for Linux Sysadmins

## Network Configuration

| Command    | Description                                              | Example                           |
|------------|----------------------------------------------------------|-----------------------------------|
| `ifconfig` | Configures a network interface (deprecated)              | `ifconfig eth0 192.168.1.10`      |
| `ip`       | Shows/manages routing, devices, policy routing, tunnels  | `ip addr show`                    |
| `ip link`  | Displays and manages network interfaces                  | `ip link set eth0 up`             |
| `ip route` | Displays and manipulates routing table                   | `ip route add default via 192.168.1.1` |

## Network Diagnostics

| Command         | Description                                               | Example                            |
|-----------------|-----------------------------------------------------------|------------------------------------|
| `ping`          | Sends ICMP ECHO_REQUEST to network hosts                  | `ping google.com`                  |
| `traceroute`    | Traces the route packets take to a network host           | `traceroute google.com`            |
| `tracepath`     | Similar to traceroute but doesn't require superuser rights| `tracepath google.com`             |
| `mtr`           | Combines ping and traceroute functionality                | `mtr google.com`                   |
| `netstat`       | Prints network connections, routing tables, interface stats | `netstat -tuln`                    |
| `ss`            | Investigates sockets                                       | `ss -tuln`                         |
| `dig`           | Queries DNS name servers                                   | `dig example.com`                  |
| `nslookup`      | Queries DNS to obtain domain name or IP address mapping    | `nslookup example.com`             |
| `host`          | DNS lookup utility                                         | `host example.com`                 |

## Network Monitoring

| Command      | Description                                             | Example                            |
|--------------|---------------------------------------------------------|------------------------------------|
| `tcpdump`    | Captures network packets                                | `tcpdump -i eth0`                  |
| `wireshark`  | GUI network protocol analyzer                           | `wireshark` (needs X server)       |
| `iftop`      | Displays bandwidth usage on an interface by host        | `iftop -i eth0`                    |
| `nload`      | Shows network traffic and bandwidth usage               | `nload eth0`                       |
| `bmon`       | Bandwidth monitor and rate estimator                    | `bmon`                             |
| `vnstat`     | Network traffic monitor                                 | `vnstat`                           |
| `iptraf-ng`  | Network monitoring utility                              | `iptraf-ng`                        |

## Network Services

| Command       | Description                                              | Example                            |
|---------------|----------------------------------------------------------|------------------------------------|
| `systemctl`   | Manages system services                                  | `systemctl restart networking`     |
| `service`     | Controls the status of system services                   | `service networking restart`       |
| `hostnamectl` | Controls the system hostname                             | `hostnamectl set-hostname newname` |
| `nmcli`       | Command-line client for NetworkManager                   | `nmcli device show`                |
| `nmtui`       | Text user interface for NetworkManager                   | `nmtui`                            |
| `dhclient`    | Dynamic Host Configuration Protocol (DHCP) client        | `dhclient eth0`                    |
| `resolvectl`  | Manages DNS resolution                                  | `resolvectl status`                |

## Network File Transfer

| Command     | Description                                              | Example                            |
|-------------|----------------------------------------------------------|------------------------------------|
| `scp`       | Securely copies files between hosts                      | `scp file.txt user@remote:/path`   |
| `sftp`      | Secure file transfer program                             | `sftp user@remote`                 |
| `rsync`     | Fast, versatile, remote (and local) file-copying tool    | `rsync -avz /source/ user@remote:/dest` |
| `curl`      | Transfers data from or to a server                       | `curl -O http://example.com/file`  |
| `wget`      | Non-interactive network downloader                       | `wget http://example.com/file`     |

## Firewall Configuration

| Command      | Description                                              | Example                            |
|--------------|----------------------------------------------------------|------------------------------------|
| `iptables`   | Administers IP packet filter rules                       | `iptables -L`                      |
| `firewalld`  | Manages firewall with zones (with firewall-cmd)          | `firewall-cmd --get-default-zone`  |
| `ufw`        | Uncomplicated Firewall, frontend for iptables            | `ufw enable`                       |

## VPN Configuration

| Command        | Description                                              | Example                            |
|----------------|----------------------------------------------------------|------------------------------------|
| `openvpn`      | OpenVPN client and server                                | `openvpn --config client.conf`     |
| `pptpsetup`    | Configures PPTP client                                   | `pptpsetup --create myvpn --server vpn.example.com --username user --password pass --encrypt` |
| `strongswan`   | IPsec-based VPN solution                                 | `strongswan start`                 |

## Miscellaneous Networking Tools

| Command       | Description                                              | Example                            |
|---------------|----------------------------------------------------------|------------------------------------|
| `ethtool`     | Displays or changes Ethernet device settings             | `ethtool eth0`                     |
| `iwconfig`    | Configures wireless network interfaces                   | `iwconfig wlan0`                   |
| `nmcli`       | Command-line client for NetworkManager                   | `nmcli device status`              |
| `iwlist`      | Lists available wireless networks                        | `iwlist wlan0 scan`                |
| `route`       | Shows/manages IP routing tables                          | `route -n`                         |
| `arp`         | Manipulates the system ARP cache                         | `arp -a`                           |
| `hostname`    | Shows or sets the system's hostname                      | `hostname`                         |
| `macchanger`  | Changes MAC address                                      | `macchanger -r eth0`               |
| `whois`       | Queries whois databases for domain registration info     | `whois example.com`                |
| `nmap`        | Network exploration tool and security/port scanner       | `nmap -sP 192.168.1.0/24`          |
| `telnet`      | User interface to the TELNET protocol                     | `telnet hostname port`             |
| `nc` (netcat) | Reads and writes data across network connections         | `nc -zv 192.168.1.1 22`            |

Feel free to use and expand this list as necessary for your needs.
