# Configuration for a local 3proxy SOCKS5 installation

To install, download or compile 3proxy and copy `3proxy.cfg` to the installation folder. Then run `$ ./3proxy.exe --install` to install as a service.

## Win32 vs Linux
There are two lines which as platform specific:
- Logs
  - Linux: `log "/var/logs/3proxy/%Y%m%d.log" D`
  - Windows: `log "%userprofile%\logs\3proxy\%Y%m%d.log" D`
- Service / Daemon:
  - Linux: `daemon`
  - Windows: `service`
  
## DNS Resolution
The config uses the privacy/security focused [Quad9](https://www.quad9.net/) for primary DNS and [Cloudflare](https://www.cloudflare.com/en-gb/dns/) for fallback.

## Configuration
You will need to replace the following tokens with your own settings before applying the config:
- `YOUR_USERNAME`: The username you want to use to set for the proxy.
- `YOUR_PASSWORD`: The plain-text password you'd like to set. _To set an encoded password refer to the 3proxy docs._
- `YOUR_INTERNAL_STATIC_IP`: The static IP address set on the interface you want to connect out via. _Example 192.168.1.xxx_ 
