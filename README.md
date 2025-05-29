# Microsoft-Blocker: Block all Microsoft Spying
### Block all network traffic to Microsoft while using Microsoft products.
#### Because how microsoft uses many of the same urls for many of their services, including their telemetry and tracking, the proper version can cause some microsoft services not to work properly. I do not use any microsoft products anymore other than vscode, so I don't get to test the microsoft blocker filters. Feel free to open a issue if the regular filter is too aggressive, or some essential services are not working. 
### [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker) is the home of Microsoft Blocker. Its mirrored at github for backup and availability. Use only one filter source. <br>Available both on [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker) and [Github](https://github.com/privacyfilters/Microsoft-Blocker).

# Most effective with Network wide firewalls, router adblockers and DNS Sinkholes. Windows can ignore host entries related to Microsoft.

## Direct DNS filters and host files links:

## Microsoft Blocker Proper: Aims to allow only minimum connections to keep windows usage reasonable.</br> Only Allows windows iso downlaod from [Massgrave.dev](https://massgrave.dev/genuine-installation-media), windows updates, winget package manager, vscode extension store and some azure related urls and some other widely used sites 
#### Adblock & DNS Filter Version- [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/adblock_dns_proper.txt) - [Github](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/refs/heads/main/adblock_dns_proper.txt)
#### Hosts version - [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/hosts) - [Github](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/refs/heads/main/hosts)
### Microsoft Blocker - No Microsoft Edition: Aims to Strictly block Eveything from and related to Microsoft </br>(Some Azure urls may not be blocked for now as they may render external services disfunctional)
#### Adblock & DNS Filter Version - [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/adblock_dns_nomicrosoft.txt) - [Github](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/refs/heads/main/adblock_dns_nomicrosoft.txt)
#### Hosts version - [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/hosts_nomicrosoft) - [Github](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/refs/heads/main/hosts_nomicrosoft)

## Recommended Method to Block Microsoft:
### Adguard Home - DNS Network-wide Adblocker - (stable)(foss)(dns) - https://github.com/AdguardTeam/AdGuardHome