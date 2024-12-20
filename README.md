**You would like to show your appreciation for our help 8-o. Gladly. We thank you for your donation! ;)**

<a href="https://www.paypal.com/donate/?hosted_button_id=JTFYJYVH37MNE">
  <img src="https://www.paypalobjects.com/en_US/i/btn/btn_donate_LG.gif">
</a>

# Ubuntu-LXC-Terminalserver-Project

Herewith I provide a lightweight graphical LXC (container) with LXQD desktop as terminal server (x2go). Ready server within a few minutes. Have fun with it :)

## Features

- LXQT with Terminalserver
- No Snap packages, everthing DEB's
- LXC Compatible with Proxmox (tested on version 7/8)
- Autoupdate and Reboot for the System (unattended-upgrades)
- Webmin: Adminstration over web on https://hostname:10000
- Samba Integration (Publicshare) configurable with Webmin
- ZSH Defaultshell
- and a lot of other nice things ;)

<img src="https://raw.githubusercontent.com/boospy/Ubuntu-LXC-Terminalserver-Project/main/screenshots/3.jpeg" width="" height="256">


## Software

- x2go Terminalserver
- OnlyOffice Suite
- tinyOTP (2Factor)
- Bitwarden
- XCA Certificatemanagement
- Kronometer
- Nextcloud Desktop
- OpenFortiGUI (VPN Client)
- MasterPDF Editor
- Draw.IO
- Brave Browser
- Firefox with Secureplugins
- Teamviewer
- Real VNCviewer
- Strawberry Musicplayer


<img src="https://raw.githubusercontent.com/boospy/Ubuntu-LXC-Terminalserver-Project/main/screenshots/2.jpeg" width="" height="256">

## Enabled Repositories
- Brave Browser
- Teamviewer
- Mozillateam Ubuntu
- ITEAS Enterpriserepo https://apt.iteas.at/


<img src="https://raw.githubusercontent.com/boospy/Ubuntu-LXC-Terminalserver-Project/main/screenshots/5.jpeg" width="" height="256">

### Minimal system requirements 
- Proxmox 8 or other LXC hostsystem
- 4 Cores
- 4GB Memory
- 15GB diskspace
- unprivileged container: "no"
- features: fuse=1

## Download
You can download the image from here:
https://sourceforge.net/projects/ubuntu-business-desktop-lxc/files/stable/

# First start

If you create the LXC, unprivileged must be deactivated.
After fist start you can login directly in the console or with ssh with root and the password that you set. The "ubd" defaultuser is enabled and you can login with password immediately with SSH and with X2GO. Password is also "ubd".

**X2go Settings**
- Session Type	LXQT
- Connection speed	recommended LAN for best quality
- Resolution	1920x1080
- Disable checkbox on "Use port forwarding over tunneling to connect audio signals across firewalls". Activating the checkbox can cause a hanging and incorrectly loading desktop environment.
- Set resolution (DPI)	79 -> only Ubuntu 20.04

The default language at the desktop is german, but you can very simple change this after login by open the regional settings:

<img src="https://raw.githubusercontent.com/boospy/Ubuntu-LXC-Terminalserver-Project/main/screenshots/change-lang01.png" width="" height="256">

and change to your prefer language. This will be applied to the desktop the next time you log in.

<img src="https://raw.githubusercontent.com/boospy/Ubuntu-LXC-Terminalserver-Project/main/screenshots/change-lang02.png" width="" height="256">


## Other settings:
You can change apt-cacher in

```
/etc/apt/apt.conf.d/01proxy
```

to your own for your apt-cacher or Squid DEB Proxy address.

Automatic Updates are configured to run in background every 7 days. Autoreboot (without users logged in) when necessary at 02:00 AM. You can change the preconfigured settings at the files:

```
/etc/apt/apt.conf.d/20periodic
/etc/apt/apt.conf.d/50unattended-upgrades
```

<img src="https://raw.githubusercontent.com/boospy/Ubuntu-LXC-Terminalserver-Project/main/screenshots/22.png" width="" height="256">

## Helpfull Links for special configuration
- [Extended Domain Services Univention for LXC or other systems without network-manager](https://docs.software-univention.de/ext-domain/5.0/en/index.html)
- [Kerberos Keytab erstellen und Debug in UCS](https://deepdoc.at/dokuwiki/doku.php?id=prebuilt_systems:ucs:kerberos_keytab_erstellen_und_debug_in_ucs)
