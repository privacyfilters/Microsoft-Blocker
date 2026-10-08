# Microsoft Blocker: Block All Microsoft Spying

**Block all network traffic to Microsoft while using Microsoft products.**

Microsoft Blocker is a collection of filters for blocking Microsoft services, telemetry, tracking, analytics, and other Microsoft-related network connections. Blocking Microsoft completely is the ultimate goal.

There are three versions available depending on how much Microsoft functionality you want to keep:

* 🟢 **Lite** — less aggressive, keeps some Microsoft services working
* 🟠 **Proper** — stronger blocking while keeping essential Windows functionality
* 🔴 **No Microsoft** — strict blocking for users who want to avoid Microsoft as much as possible

---

## ⚠️ Before You Use It

Microsoft uses many of the same domains and services for both **legitimate functionality and telemetry/tracking**. Because of this, blocking Microsoft domains can sometimes break things that you actually need.

The more aggressive the filter is, the more likely it is that some Microsoft services will stop working.

I don't use Microsoft products anymore except for **Visual Studio Code**, so I cannot personally test every Microsoft service and Windows feature.

If you find that the filter is blocking something important, or you find a Microsoft tracking/telemetry domain that is missing, please open an issue and let me know.

---

## 📍 Project Home

**Codeberg is the primary home of Microsoft Blocker.**

* **[Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker)** — Primary repository
* **[GitHub](https://github.com/privacyfilters/Microsoft-Blocker)** — Mirror

The GitHub repository is maintained as a mirror for additional availability and redundancy.

> **Please use only one copy of each filter.**
> The Codeberg and GitHub files are the same lists. Using both does not provide additional protection and only creates duplicate rules.

---

# Which Version Should I Use?

### 🟢 Microsoft Blocker Lite

**Less aggressive and more compatible.**

The Lite version blocks many Microsoft service, telemetry and tracking domains while allowing a large number of Microsoft services to continue working.

This version allows these services and domains:

* Outlook
* Microsoft Mail
* Microsoft 365 / Office
* Onedrive
* OneNote
* Teams
* Microsoft Edge Extension Store
* Some other Microsoft online services
* Allowed services in Proper version

If you want to reduce Microsoft tracking without completely breaking Microsoft services, **start with Lite**.

---

### 🟠 Microsoft Blocker Proper

**Stronger blocking with a focus on keeping Windows usable. Blocks many Microsoft Products**

The Proper version Aims to allow minimum connections to keep windows usage functional and everything else from microsoft is blocked.

It aims to allow only the Microsoft connections that are useful or necessary for a reasonably functional Windows installation, updates and some select vital services.

Currently, this version allows these services and domains:

* Windows Updates
* Windows Defender
* DotNet(.Net)
* Winget
* Github
* Linkedin
* Minecraft
* Visual Studio Code Extension Marketplace
* Some Azure-related connections
* Windows ISO downloads from [Massgrave.dev](https://massgrave.dev/genuine-installation-media)

Most other Microsoft-related connections are blocked.

### Microsoft Edge

**Microsoft Edge is not recommended with the Proper filter.**

Edge makes a large number of Microsoft-related connections, including telemetry and tracking connections. Blocking these connections can interfere with Edge.

This can also affect security-related functionality because some required Microsoft endpoints may be blocked.

---

### 🔴 Microsoft Blocker — No Microsoft

**The strictest version.**

The No Microsoft edition is intended for users who simply do not want Microsoft-related connections on their network.

There are still some Microsoft owned/related services are allowed, otherwise normal internet usage will break severly.

Allowed services includes:

* Github & Githubusercontent
* Some azure Related domains many external services depends on

> **⚠️ Azure warning:** Some Azure domains will remain unblocked. Microsoft Azure is used by many websites and services that have nothing to do with Microsoft. Blocking Azure infrastructure too aggressively can break unrelated services.

If you don't use Microsoft services and want the strongest blocking possible, this is the version to use.

---

# 🛡️ Recommended Blocking Methods

## Most effective with network-wide firewalls, router adblockers, and DNS sinkholes.

## Not Recommended: **Windows hosts files** or adblockers like **AdGuard for Windows**, as Microsoft can ignore/bypass them. They are only partially effective against telemetry.

Microsoft Blocker can be used with many different DNS, firewall, and content-blocking applications.

Choose the method that fits your setup. **The format marked "Best Method" is the format I recommend for that application.**

## 🌐 Network-wide DNS / Firewall

### AdGuard Home

[AdGuard Home](https://github.com/AdguardTeam/AdGuardHome) is a network-wide DNS blocker and one of the easiest ways to use Microsoft Blocker.

**Recommended formats:**

* **Adblock / DNS — Best Method**
* Domains
* Hosts

---

### Pi-hole

[Pi-hole](https://pi-hole.net/) is a popular network-wide DNS blocker.

**Recommended formats:**

* **Domains — Best Method**

Pi-hole can parse some other common list formats, but the Domains version is the most straightforward and predictable choice.

---

### Adblock-lean

[Adblock-lean](https://github.com/lynxthecat/adblock-lean) supports **raw/domain-only, dnsmasq, and hosts** formats. Its documentation specifically notes that raw/domain-only lists have lower processing and memory overhead, and its built-in presets primarily use raw-format lists.

**Recommended formats:**

* **Domains — Best Method**
* DNSMasq
* Hosts

---

### Adblock-Fast

[adblock-fast](https://github.com/mossdef-org/adblock-fast) is a lightweight DNS-based blocker for OpenWrt that works with dnsmasq, SmartDNS, and Unbound.

**Recommended formats:**

* **Adblock / DNS — Best Method**
* Domains
* Hosts

---

### pfSense + pfBlockerNG

[pfBlockerNG](https://pfblockerng.com/) is a popular DNS and firewall blocking package for [pfSense](https://www.pfsense.org/).

Its DNSBL feature supports domain, hosts-style, and Adblock Plus/EasyList sources.

**Recommended formats:**

* **Adblock / DNS — Best Method**
* Domains
* Hosts

---

### OPNsense

[OPNsense](https://opnsense.org/) includes built-in DNS blocklist support through its Unbound DNS resolver.

**Recommended formats:**

* **Domains — Best Method**

---

## 🌍 Browser / Application-level Blocking

### uBlock Origin

[uBlock Origin](https://github.com/gorhill/uBlock) can use the Adblock / DNS versions of Microsoft Blocker for browser-level Microsoft blocking.

**Recommended formats:**

* **Adblock / DNS — Best Method**

> Browser-level blocking only affects supported browser traffic. It cannot block Microsoft connections made directly by other applications.

---

### Brave Shields

[Brave Shields](https://brave.com/shields/) is Brave's built-in browser content blocker. It supports its own filter lists based on **uBlock Origin/Adblock-style syntax**.

**Recommended format:**

* **Adblock / DNS — Best Method**

---

## 📱 Android

### personalDNSfilter

[personalDNSfilter](https://github.com/IngoZenz/personaldnsfilter) is an Android DNS-based filter that supports remote hosts-style filter lists.

**Recommended formats:**

* **Hosts — Best Method**

---

### AdAway

[AdAway](https://adaway.org/) is an Android ad blocker that can use hosts-based blocklists.

**Recommended formats:**

* **Hosts — Best Method**
* Domains

For AdAway, **Hosts** is the preferred format because it is designed to work directly with hosts-style blocking lists.

---

### AdGuard for Android

[AdGuard for Android](https://adguard.com/en/adguard-android/overview.html) supports Adblock-style filtering and DNS-based blocking.

**Recommended formats:**

* **Adblock / DNS — Best Method**
* Domains
* Hosts

---

## 📋 Quick Reference

| Application               | Type                     | Best Method   | Opensource |
| ------------------------- | ------------------------ | ------------- | :--------: |
| **AdGuard Home**          | Network-wide DNS blocker | Adblock / DNS |      ✅     |
| **Pi-hole**               | Network-wide DNS blocker | Domains       |      ✅     |
| **Adblock-lean**          | OpenWrt DNS blocker      | Domains       |      ✅     |
| **Adblock-Fast**          | OpenWrt DNS blocker      | Adblock / DNS |      ✅     |
| **pfSense + pfBlockerNG** | Firewall / DNS blocker   | Adblock / DNS |     ⚠️     |
| **OPNsense**              | Firewall / DNS blocker   | Domains       |      ✅     |
| **uBlock Origin**         | Browser content blocker  | Adblock / DNS |      ✅     |
| **Brave Shields**         | Browser content blocker  | Adblock / DNS |     ⚠️     |
| **personalDNSfilter**     | Android DNS blocker      | Hosts         |      ✅     |
| **AdAway**                | Android hosts blocker    | Hosts         |      ✅     |
| **AdGuard for Android**   | Android system blocker   | Adblock / DNS |      ❌     |

---

# 🚫 What About Windows Hosts Files?

I don't recommend relying only on a Windows hosts file for Microsoft blocking.

Microsoft applications can use different network paths and mechanisms, so hosts-file blocking may only provide partial protection.

The same applies to desktop-level ad blockers such as AdGuard for Windows. They can block a lot of Microsoft traffic, but they cannot necessarily prevent every connection made by Microsoft software.

For better coverage, **use Microsoft Blocker at the DNS/network level**.

---

# 📥 Filter Lists

## 🟢 Microsoft Blocker Lite

Less aggressive version. Recommended if you still need Microsoft services such as Outlook, Office, etc.

### Adblock / DNS

* [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/adblock_dns_lite.txt)
* [GitHub](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/adblock_dns_lite.txt)

### Domains

* [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/domains_lite.txt)
* [GitHub](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/domains_lite.txt)

### DNSMasq

* [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/dnsmasq_lite.txt)
* [GitHub](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/dnsmasq_lite.txt)

### Hosts

* [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/hosts_lite)
* [GitHub](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/hosts_lite)

---

# 🟠 Microsoft Blocker Proper

Stronger blocking while keeping selected Windows functionality working. Allows Windows ISO downloads from [Massgrave.dev](https://massgrave.dev/genuine-installation-media), Windows Updates, Winget package manager, VS Code Extension Marketplace, and some Azure-related URLs.

### Adblock / DNS

* [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/adblock_dns_proper.txt)
* [GitHub](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/adblock_dns_proper.txt)

### Domains

* [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/domains.txt)
* [GitHub](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/domains.txt)

### DNSMasq

* [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/dnsmasq.txt)
* [GitHub](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/dnsmasq.txt)

### Hosts

* [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/hosts)
* [GitHub](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/hosts)

### Hosts-clean

The same filter as the regular hosts file, but without the extra comments.

Useful if you want a cleaner hosts file and a hosts file with a different name (Adblock-lean shows an error when adding the normal `hosts` file).

* [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/hosts-clean)
* [GitHub](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/hosts-clean)

---

# 🔴 Microsoft Blocker — No Microsoft

The strictest version. Intended for users who want to block Microsoft as much as possible. Some Azure URLs may not be blocked for now as they may render external services dysfunctional, since many services other than Microsoft use Azure cloud infrastructure.

### Adblock / DNS

* [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/adblock_dns_nomicrosoft.txt)
* [GitHub](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/adblock_dns_nomicrosoft.txt)

### Domains

* [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/domains_nomicrosoft.txt)
* [GitHub](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/domains_nomicrosoft.txt)

### DNSMasq

* [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/dnsmasq.txt)
* [GitHub](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/dnsmasq.txt)

### Hosts

* [Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/hosts_nomicrosoft)
* [GitHub](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/hosts_nomicrosoft)

---

# 📋 Filter Formats

| Format            | Intended Use                             |
| ----------------- | ---------------------------------------- |
| **Adblock / DNS** | AdGuard, browser blockers, DNS filtering |
| **Domains**       | DNS blocklists and domain-based blockers |
| **DNSMasq**       | OpenWrt, dnsmasq, and compatible systems |
| **Hosts**         | Hosts-file-based blocking                |
| **Hosts-clean**   | Hosts file without extra comments        |

Use the format that is supported by your blocking software.

---

# ⚠️ Possible Breakage

Microsoft owns a huge amount of infrastructure, and some Microsoft services share infrastructure with other services.

This is especially important with **Azure**.

A blocked domain might be used for:

* Microsoft telemetry
* Microsoft authentication
* Software downloads
* Windows Updates
* Microsoft APIs
* Cloud services
* Third-party services hosted on Azure

Because of this, **a Microsoft blocker cannot guarantee that everything Microsoft-related can be blocked without causing some breakage**.

If something stops working, please check your DNS/adblock logs first and find out which domain was blocked.

Then open an issue with:

1. The blocked domain
2. Which filter you are using
3. The application or service that stopped working
4. Any useful error message

This makes it much easier to determine whether the domain should remain blocked or be allowed.

---

# 🤝 Contributing

Issues and testing reports are welcome.

Please let me know if you find:

* Missing Microsoft root domains
* Missing Microsoft telemetry domains
* Missing Microsoft tracking domains
* False positives
* Microsoft services that are unnecessarily blocked
* Microsoft domains that are no longer used
* Important Windows functionality that stops working

If possible, include the exact domain and the application/service that uses it.

---

# ⭐ Related Lists

If you **don't need aggressive Microsoft blocking** and only want general Microsoft tracking protection, you may be better off using established tracker lists instead.

* [HaGeZi DNS Blocklists — Native Trackers: Microsoft](https://github.com/hagezi/dns-blocklists#native)
* [celenity — BadBlock Microsoft](https://codeberg.org/celenity/BadBlock#individual-lists)

Microsoft Blocker is intended for users who want **much stronger Microsoft-specific blocking** rather than just basic tracker protection.

---