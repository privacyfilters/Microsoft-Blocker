# Microsoft Blocker: Block All Microsoft Spying

**Block all network traffic to Microsoft while using Microsoft products.**

Microsoft Blocker is a collection of filters for blocking Microsoft services, telemetry, tracking, analytics, and other Microsoft-related network connections. Blocking Microsoft completely is the ultimate goal.

There are three versions, depending on how much Microsoft functionality you want to keep:

* 🟢 **[Lite](#filter-lite)**: less aggressive, keeps some Microsoft services working
* 🟠 **[Proper](#filter-proper)**: stronger blocking while keeping essential Windows functionality
* 🔴 **[No Microsoft](#filter-no-microsoft)**: strict blocking for users who want to avoid Microsoft as much as possible

---

## ⚠️ Before You Use It

Microsoft uses many of the same domains and services for both **legitimate functionality and telemetry/tracking**. Because of this, blocking Microsoft domains can sometimes break things you actually need. The more aggressive the filter, the more likely it is that some Microsoft services will stop working.

I don't use Microsoft products anymore except for **Visual Studio Code**, so I can't personally test every Microsoft service and Windows feature.

If a filter blocks something important, or you find a Microsoft tracking/telemetry domain that's missing, please open an issue and let me know (see [Possible Breakage](#️-possible-breakage)).

These filters work best with **network-wide firewalls, router adblockers, and DNS sinkholes**. See [Recommended Blocking Methods](#️-recommended-blocking-methods) below.

---

## 📍 Project Home

**Codeberg is the primary home of Microsoft Blocker.**

* **[Codeberg](https://codeberg.org/privacyfilters/Microsoft-Blocker)**: primary repository
* **[GitHub](https://github.com/privacyfilters/Microsoft-Blocker)**: mirror, kept for additional availability and redundancy

> **Please use only one copy of each filter.**
> The Codeberg and GitHub files are the same lists. Using both doesn't give you extra protection, it only creates duplicate rules.

---

# 🧭 Which Version Should I Use?

| Version | Blocking | Best for |
| ------- | -------- | -------- |
| 🟢 **[Lite](#filter-lite)** | Light | Keeping Outlook, Office, OneDrive, Teams and similar services working |
| 🟠 **[Proper](#filter-proper)** | Strong | A functional Windows install with updates, with most other Microsoft connections blocked |
| 🔴 **[No Microsoft](#filter-no-microsoft)** | Strictest | People who don't want any Microsoft connections on their network |

## 🟢 Microsoft Blocker Lite

**Less aggressive and more compatible.**

Lite blocks many Microsoft service, telemetry and tracking domains while allowing a large number of Microsoft services to keep working.

**Allowed services and domains:**

* Outlook
* Microsoft Mail
* Microsoft 365 / Office
* OneDrive
* OneNote
* Teams
* Microsoft Edge Extension Store
* Some other Microsoft online services
* Things that are allowed in Proper version

If you want to reduce Microsoft tracking without completely breaking Microsoft services, **start with Lite**.

---

## 🟠 Microsoft Blocker Proper

**Stronger blocking with a focus on keeping Windows usable. Blocks many Microsoft products.**

Proper allows the minimum connections needed to keep Windows functional, and blocks most other Microsoft connections. It only allows what's useful or necessary for a reasonably functional Windows installation, updates, and some select vital services.

**Currently allowed services and domains:**

* Windows Updates
* Windows Defender
* .NET
* Winget
* GitHub
* LinkedIn
* Minecraft
* Visual Studio Code Extension Marketplace
* Some Azure-related connections
* Windows ISO downloads from [Massgrave.dev](https://massgrave.dev/genuine-installation-media)

Most other Microsoft-related connections are blocked.

> **Microsoft Edge is not recommended with the Proper filter.**
> Edge makes a large number of Microsoft-related connections, including telemetry and tracking. Blocking them can interfere with Edge, and it can also affect security-related functionality because some required Microsoft endpoints may be blocked.

---

## 🔴 No Microsoft Edition

**The strictest version.**

No Microsoft is for users who simply don't want Microsoft-related connections on their network. A few Microsoft-owned or Microsoft-related services are still allowed, otherwise normal internet usage can break severely.

**Allowed services:**

* GitHub and githubusercontent
* Some Azure-related domains that many external services depend on

> **⚠️ Azure warning:** Some Azure domains stay unblocked. Microsoft Azure is used by many websites and services that have nothing to do with Microsoft, and blocking Azure infrastructure too aggressively can break unrelated services.

If you don't use Microsoft services and want the strongest blocking possible, this is the version to use.

---

# 📥 Filter Lists

<a id="filter-lite"></a>

## 🟢 Lite

Less aggressive version. Recommended if you still need Microsoft services such as Outlook, Office, OneDrive, OneNote, Teams, etc.

| Format | Works with | Codeberg | GitHub |
| ------ | ---------- | -------- | ------ |
| **Adblock / DNS** | AdGuard Home, Adblock-Fast, pfSense + pfBlockerNG, uBlock Origin, Brave Shields, AdGuard for Android | [Link](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/adblock_dns_lite.txt) | [Link](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/adblock_dns_lite.txt) |
| **Domains** | Pi-hole, OPNsense, Adblock-lean, AdAway | [Link](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/domains_lite.txt) | [Link](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/domains_lite.txt) |
| **DNSMasq** | DNSMasq, Adblock-lean (OpenWrt) | [Link](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/dnsmasq_lite.txt) | [Link](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/dnsmasq_lite.txt) |
| **Hosts** | personalDNSfilter, AdAway, hosts-file-based blockers | [Link](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/hosts_lite) | [Link](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/hosts_lite) |

---

<a id="filter-proper"></a>

## 🟠 Proper

Stronger blocking while keeping selected Windows functionality working. Allows Windows ISO downloads from [Massgrave.dev](https://massgrave.dev/genuine-installation-media), Windows Updates, the Winget package manager, the VS Code Extension Marketplace, and some Azure-related URLs.

| Format | Works with | Codeberg | GitHub |
| ------ | ---------- | -------- | ------ |
| **Adblock / DNS** | AdGuard Home, Adblock-Fast, pfSense + pfBlockerNG, uBlock Origin, Brave Shields, AdGuard for Android | [Link](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/adblock_dns_proper.txt) | [Link](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/adblock_dns_proper.txt) |
| **Domains** | Pi-hole, OPNsense, Adblock-lean, AdAway | [Link](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/domains.txt) | [Link](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/domains.txt) |
| **DNSMasq** | DNSMasq, Adblock-lean (OpenWrt) | [Link](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/dnsmasq.txt) | [Link](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/dnsmasq.txt) |
| **Hosts** | personalDNSfilter, AdAway, hosts-file-based blockers | [Link](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/hosts) | [Link](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/hosts) |
| **Hosts-clean** | Adblock-lean. Identical to Hosts, just with a different name (use it if `hosts` causes an error) | [Link](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/hosts-clean) | [Link](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/hosts-clean) |

---

<a id="filter-no-microsoft"></a>

## 🔴 No Microsoft

The strictest version, for users who want to block Microsoft as much as possible. Some Azure URLs may stay unblocked for now, since they could break external services: many services other than Microsoft's use Azure cloud infrastructure.

| Format | Works with | Codeberg | GitHub |
| ------ | ---------- | -------- | ------ |
| **Adblock / DNS** | AdGuard Home, Adblock-Fast, pfSense + pfBlockerNG, uBlock Origin, Brave Shields, AdGuard for Android | [Link](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/adblock_dns_nomicrosoft.txt) | [Link](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/adblock_dns_nomicrosoft.txt) |
| **Domains** | Pi-hole, OPNsense, Adblock-lean, AdAway | [Link](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/domains_nomicrosoft.txt) | [Link](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/domains_nomicrosoft.txt) |
| **DNSMasq** | DNSMasq, Adblock-lean (OpenWrt) | [Link](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/dnsmasq.txt) | [Link](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/dnsmasq.txt) |
| **Hosts** | personalDNSfilter, AdAway, hosts-file-based blockers | [Link](https://codeberg.org/privacyfilters/Microsoft-Blocker/raw/branch/main/hosts_nomicrosoft) | [Link](https://raw.githubusercontent.com/privacyfilters/Microsoft-Blocker/main/hosts_nomicrosoft) |

---

# 🛡️ Recommended Blocking Methods

Microsoft Blocker works best with **network-wide firewalls, router adblockers, and DNS sinkholes**. Pick the method that fits your setup. The format in **bold** is the one I recommend for that application.

> **Not recommended:** Windows hosts files, or adblockers like AdGuard for Windows. Microsoft can ignore or bypass them, so they're only partially effective against telemetry. See [What About Windows Hosts Files?](#-what-about-windows-hosts-files) below.

## 🌐 Network-wide (most recommended)

| Tool | Type | Format | FOSS | Notes |
| ---- | ---- | ------ | :--: | ----- |
| **[AdGuard Home](https://github.com/AdguardTeam/AdGuardHome)** | DNS network-wide blocker | **Adblock / DNS**, Domains, Hosts | ✅ | One of the easiest ways to use Microsoft Blocker. Windows, Linux, macOS, OpenWrt |
| **[Pi-hole](https://pi-hole.net/)** | DNS network-wide blocker | **Domains** | ✅ | Can parse some other common formats, but Domains is the most straightforward and predictable |
| **[Adblock-lean](https://github.com/lynxthecat/adblock-lean)** | Router blocker (OpenWrt only) | **Domains**, DNSMasq, Hosts | ✅ | Raw/domain-only lists have lower processing and memory overhead, and its built-in presets mostly use them. Use Hosts-clean, as plain `hosts` gives an error |
| **[Adblock-Fast](https://github.com/mossdef-org/adblock-fast)** | Router blocker (OpenWrt only) | **Adblock / DNS**, Domains, Hosts | ✅ | Lightweight. Works with dnsmasq, SmartDNS and Unbound |
| **[pfSense + pfBlockerNG](https://pfblockerng.com/)** | Firewall / DNS blocker | **Adblock / DNS**, Domains, Hosts | ⚠️ | DNSBL supports domain, hosts-style and Adblock Plus/EasyList sources. pfSense is not fully open source |
| **[OPNsense](https://opnsense.org/)** | Firewall / DNS blocker | **Domains** | ✅ | Built-in DNS blocklist support through the Unbound DNS resolver |

## 🌍 Browser / Application-level

| Tool | Type | Format | FOSS | Notes |
| ---- | ---- | ------ | :--: | ----- |
| **[uBlock Origin](https://github.com/gorhill/uBlock)** | Browser content blocker | **Adblock / DNS** | ✅ | Browser traffic only |
| **[Brave Shields](https://brave.com/shields/)** | Browser content blocker | **Adblock / DNS** | ⚠️ | Brave's built-in blocker, uses uBlock Origin/Adblock-style syntax. Browser traffic only |

> Browser-level blocking only affects supported browser traffic. It can't block Microsoft connections made directly by other applications.

## 📱 Android

| Tool | Type | Format | FOSS | Notes |
| ---- | ---- | ------ | :--: | ----- |
| **[personalDNSfilter](https://github.com/IngoZenz/personaldnsfilter)** | DNS filter | **Hosts** | ✅ | Supports remote hosts-style filter lists |
| **[AdAway](https://adaway.org/)** | Hosts-based adblocker | **Hosts**, Domains | ✅ | Hosts is preferred because it's designed to work directly with hosts-style lists |
| **[AdGuard for Android](https://adguard.com/en/adguard-android/overview.html)** | System-wide blocker | **Adblock / DNS**, Domains, Hosts | ❌ | Paid app. Supports Adblock-style filtering and DNS-based blocking |

## 💻 Windows (not recommended)

| Tool | Type | Format | FOSS | Notes |
| ---- | ---- | ------ | :--: | ----- |
| **Windows hosts file** | Manual hosts file editing | Hosts | n/a | ⚠️ Only partial protection |
| **[AdGuard for Windows](https://adguard.com/en/adguard-windows/overview.html)** | Desktop-level adblocker | Adblock / DNS | ❌ | ⚠️ Paid app. Only partial protection |

---

# 📝 Notes on Compatibility

* The **Adblock / DNS** format works perfectly on AdGuard Home, and is the best choice for Adblock-Fast, pfBlockerNG and browser blockers.
* **Hosts** rules work anywhere that supports the hosts format, on any platform.
* **Domains** is the best choice for Pi-hole, OPNsense and Adblock-lean.
* **Adblock-lean on OpenWrt:** Domains, DNSMasq and Hosts-clean all work (plain `hosts` gives an error). Domains has the lowest overhead.
* **DNSMasq** is for OpenWrt, dnsmasq, and compatible systems.

---

# 🚫 What About Windows Hosts Files?

I don't recommend relying only on a Windows hosts file for Microsoft blocking.

Microsoft applications can use different network paths and mechanisms, so hosts-file blocking may only give partial protection.

The same goes for desktop-level ad blockers such as AdGuard for Windows. They can block a lot of Microsoft traffic, but they can't necessarily stop every connection made by Microsoft software.

For better coverage, **use Microsoft Blocker at the DNS/network level**.

---

# ⚠️ Possible Breakage

Microsoft owns a huge amount of infrastructure, and some Microsoft services share infrastructure with other services. This is especially true of **Azure**.

A blocked domain might be used for:

* Microsoft telemetry
* Microsoft authentication
* Software downloads
* Windows Updates
* Microsoft APIs
* Cloud services
* Third-party services hosted on Azure

Because of this, **a Microsoft blocker can't guarantee that everything Microsoft-related gets blocked without some breakage**.

If something stops working, check your DNS/adblock logs first and find out which domain was blocked. Then open an issue with:

1. The blocked domain
2. Which filter you're using
3. The application or service that stopped working
4. Any useful error message

This makes it much easier to decide whether the domain should stay blocked or be allowed.

---

# 🤝 Contributing

Issues and testing reports are welcome. Please let me know if you find:

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

If you **don't need aggressive Microsoft blocking** and only want general Microsoft tracking protection, you may be better off with established tracker lists:

* [HaGeZi DNS Blocklists: Native Trackers, Microsoft](https://github.com/hagezi/dns-blocklists#native)
* [celenity BadBlock: Microsoft](https://codeberg.org/celenity/BadBlock#individual-lists)

Microsoft Blocker is for users who want **much stronger Microsoft-specific blocking** than basic tracker protection.

---

# 🔗 All Sources and Mirrors

* **Codeberg:** https://codeberg.org/privacyfilters/Microsoft-Blocker
* **GitHub (mirror):** https://github.com/privacyfilters/Microsoft-Blocker