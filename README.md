# NoNagProxmox
> A Somewhat Professional fork of [pve-fake-subscription](https://github.com/Jamesits/pve-fake-subscription)

Disables the "No valid subscription" dialog on all Proxmox products.

Note: This is intended for Homelabbers and not Companys that have the money to buy a Subscription,

if you can please support Proxmox and buy one!

## Features

Works for:

- Proxmox VE (5.x or later, tested up to 8.x)
- Proxmox Mail Gateway (5.x or later)
- Proxmox Backup Server (1.x)

Highlights:

- Non-intrusive: zero modification of any system file
- Future-proof: persists between system updates & major upgrades
- Hassle-free: you can uninstall at any time
- Comes with standard Debian package, easy to manage and automate
- Configurable: Product Name & PBS Message. See folder /etc/NoNagProxmox on your host

## Installation / Usage

1. [Download the latest release](https://github.com/Games-Crack/NoNagProxmox/releases)
1. Install: run `apt install NoNagProxmox_\*.deb` as root on every node

Notes:

After installation, please refrain yourself from clicking the "check" button on the "Subscription" page. It will invalidate the cache and temporary revert your instance into an unlicensed status.

The fake subscription status doesn't grant you free access to the enterprise repository. You should switch to the no-subscription repository if not already done. Use the following method:

- [Proxmox VE (PVE)](https://pve.proxmox.com/wiki/Package_Repositories#sysadmin_no_subscription_repo)
- [Proxmox Mail Gateway (PMG)](https://pmg.proxmox.com/pmg-docs/pmg-admin-guide.html#pmg_package_repositories)
- [Proxmox Backup Server (PBS)](https://pbs.proxmox.com/docs/installation.html#proxmox-backup-no-subscription-repository)

## Uninstallation

Run as root:

```shell
apt purge NoNagProxmox
```

This will revert your system to a "no subscription key" status.

## Building the Package

Install [nFPM](https://nfpm.goreleaser.com/install/), then:

```shell
./package.sh
```


## Disclaimer

This project, its author, and all associated entities have no direct affiliation or formal relationship with Proxmox or Maurer IT. Any representations or suggestions otherwise are purely coincidental. 

The creator of this project operates independently, without endorsement or approval from Proxmox or Maurer IT. The project has been developed and is being maintained without any form of official collaboration or partnership with Proxmox or Maurer IT. 

Any trademarks, service marks, trade names, or logos mentioned or used belong to their respective owners. They are used solely for the purpose of identification or clarification, without any intent to infringe on the rights of the trademark owners.

Please be aware that any actions, views, opinions, or recommendations put forward by this project and its author are entirely their own and do not reflect the views or policies of Proxmox or Maurer IT. 

Your use of this project is at your own risk, and neither Proxmox nor Maurer IT will be held responsible or liable for any harm or damages that may arise from your use of the project. 
