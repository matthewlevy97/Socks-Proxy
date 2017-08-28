# Socks-Proxy
A Socks proxy server (versions 4a and 5) in Python2.7.
This project is still a work in progress

# Setup
python ./socksProxy.py

# TODO
- Add support for bind requests in version 4 and 5
- Add UDP support for version 5
- Add support for simple VPN setup
- Add config file support
- Add ability to block outgoing requests to certain regions
- Add DNS caching

# VPN
The purpose for this feature will be to allow for secure communication on a non-secure network. Socks Proxies only relay traffic, so if browsing the web via HTTP (instead of HTTPS) your traffic will still not be encrypted regardless of proxing the data. This feature is currently not implemented.
- User runs the socks server on their local computer and runs another socks server on a remote computer
- User configures local socks server to route traffic to remote socks server
- Local socks server encrypts all outbound traffic using SSL
- Remote socks server decrypts traffic and forwards it like a normal socks proxy
- When data is returning, traffic is SSL encrypted by remote socks and decrypted by local

# Extra
- Follows the specs from https://en.wikipedia.org/wiki/SOCKS.
