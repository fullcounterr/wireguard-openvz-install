# WireGuard installer

**This project is a modified script from [angristan](https://github.com/angristan/wireguard-install) to support Ubuntu on OpenVZ for my personal use!**
**Manual installation of other distros available on [Daniel15](https://d.sb/2019/07/wireguard-on-openvz-lxc) site**

WireGuard is a point-to-point VPN that can be used in different ways. Here, we mean a VPN as in: the client will forward all its traffic trough an encrypted tunnel to the server.
The server will apply NAT to the client's traffic so it will appear as if the client is browsing the web with the server's IP.

The script supports both IPv4 and IPv6.  This has been tested on Ubuntu 18.04.4 LTS running on OpenVZ 7

## Requirements

Supported distributions:

- Ubuntu >= 16.04

## Usage

Download and execute the script. Answer the questions asked by the script and it will take care of the rest.

```bash
curl -O https://raw.githubusercontent.com//fullcounterr/wireguard-openvz-install/master/wireguard-install.sh
chmod +x wireguard-install.sh
./wireguard-install.sh
```

It will install WireGuard-go (userspace) on the server, configure it, create a systemd service and a client configuration file.

Run the script again to add or remove clients!
