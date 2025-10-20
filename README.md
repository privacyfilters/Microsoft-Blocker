# Microsoft-Blocker: Block all Microsoft Spying
### Block all network traffic to Microsoft while using Microsoft products.
#### Because how microsoft uses many of the same urls for many of their services, including their telemetry and tracking, the proper version can cause some microsoft services not to work properly. I do not use any microsoft products anymore other than vscode, so I don't get to test the microsoft blocker filters. Feel free to open an issue if the regular filter is too aggressive, or some essential services are not working. 
### [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker) is the home of Microsoft Blocker. Its mirrored at github for backup and availability. Use only one filter source. <br>Available both on [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker) and [Github](https://github.com/privacyfilters/Microsoft-Blocker)(mirror).

## Microsoft Blocker filters is focused on blocking all Microsoft Spying. If you only need minimal tracking protection, you should use [Hegezi](https://github.com/hagezi/dns-blocklists)'s [Native Trackers:Microsoft](https://github.com/hagezi/dns-blocklists?tab=readme-ov-file#native) and [celenity](https://codeberg.org/celenity/)'s [Badblock Microsoft individual list](https://codeberg.org/celenity/BadBlock#individual-lists).

# Most effective with Network wide firewalls, router adblockers and DNS Sinkholes. Windows can ignore host entries related to Microsoft.

## Direct DNS filters and host files links:

## Microsoft Blocker Proper: Aims to allow minimum connections to keep windows usage functional. Allows windows iso downoad from [Massgrave.dev](https://massgrave.dev/genuine-installation-media).
Only Allows windows iso downlaod from [Massgrave.dev](https://massgrave.dev/genuine-installation-media), windows updates, winget package manager, vscode extension store and some azure related urls. Usage of Microsoft Edge is not recommended as any connection from edge is blocked. This blocks all tracking connection from edge, which edge makes as much as an entire windows os(even on linux!). But blocking edge conneciton will make it less secure.
### Microsoft Blocker Proper: Adblock & DNS Filter Version- [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/adblock_dns_proper.txt) - [Github](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/refs/heads/main/adblock_dns_proper.txt)
### Microsoft Blocker Proper: Hosts version - [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/hosts) - [Github](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/refs/heads/main/hosts)
## Microsoft Blocker - No Microsoft Edition: Aims to Strictly block Eveything from and related to Microsoft. 
Some Azure urls may not be blocked for now as they may render external services disfunctional.Since many services other than microsoft uses azure cloud.
### Microsoft Blocker - No Microsoft: Adblock & DNS Filter Version - [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/adblock_dns_nomicrosoft.txt) - [Github](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/refs/heads/main/adblock_dns_nomicrosoft.txt)
### Microsoft Blocker - No Microsoft: Hosts version - [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/hosts_nomicrosoft) - [Github](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/refs/heads/main/hosts_nomicrosoft)

## Recommended Method to Block Microsoft:
### Adguard Home - DNS Network-wide Adblocker - (stable)(foss)(dns) - https://github.com/AdguardTeam/AdGuardHome