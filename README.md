# FAKE MESHO SCAM – Investigation Summary

This repository documents a detailed investigation into a fraudulent website impersonating **Meesho**, including Indicators of Compromise (IOC), DNS/IP attribution, and forensic metadata.  

---

## 🔍 Indicators of Compromise (IOC)

**Suspicious YouTube Channel**  
- [Meeshosalesoffer](https://www.youtube.com/@Meeshosalesoffer) – used to lure victims

**Fraudulent Sites & Redirects**  
- Google redirect: `https://www.googleadservices.com/pagead/aclk?...`  
- Main fake site: [xoofi.shop](https://xoofi.shop)

---

## 🌐 DNS & IP Details

**Nameservers for xoofi.shop**  
- `ns1.dns-parking.com`  
- `ns2.dns-parking.com`  

**Related IP Addresses**  
- `37.209.194.4`  
- `82.25.120.19`  

---

## 🏢 Domain & Infrastructure Data

- **Registrar:** Hostinger Operations, UAB  
- **WHOIS Server:** whois.hostinger.com  
- **Registrar Abuse Contact:** abuse@hostinger.com  
- **Domain Creation Date:** 2025-09-01  
- **Domain Expiry Date:** 2026-09-01  
- **Domain Status:** clientTransferProhibited, addPeriod  
- **DNSSEC:** Unsigned  
- **Registrant Country:** US  

---

## 📱 QR Code Downloaded from Site

Hashes for QR code (tested in controlled environment, **non-malicious**):  

| Hash Type | Value |
|-----------|-------|
| MD5       | 4aa5e4adfd97444acba19f53b1180da9 |
| SHA256    | 49be5659d85383797f1ff4017e39c916111d63d2c11129f6c79b68c9feaffefe |
| SHA1      | 35f872c3653d1002a9e39eabdff881fc7beca03 |

---

## 🌍 IP Address Attribution

1. **37.209.194.4 – Indonesia (Telkomsel)**  
   - Provider: PT.TELKOMSEL Indonesia  
   - Netname: TELKOMSELNET-ID  
   - Address: Telkom Landmark Tower, Jakarta, Indonesia  
   - Abuse Contact: hostmaster@telkomsel.co.id  
   - Status: Allocated Portable  
   - Route: 39.209.0.0/16 (AS23693, Jakarta)  
   - Remarks: Abuse validated on 2025-05-22  

2. **82.25.120.19 – Mumbai, India**  
   - Provider: HOSTINGER Hosting  
   - Netname: HOSTINGER-HOSTING  
   - Geo Location: 19.076090, 72.877426  
   - Organization: Private Customer (Country: Cyprus)  
   - Abuse Contact: report@abuseradar.com  
   - Route: 82.25.120.0/21 (AS47583, HOSTINGER IN)  
   - Status: Assigned PA  
   - Address: Private Residence, Cyprus  
   - Created: 2025-02-04 (last modified: 2025-02-21)  

---

## Investigation Methodology

While scrolling through social media, I came across an advertisement promoting extremely cheap devices—such as a Galaxy Fold for just ₹500—which immediately raised suspicion. Upon visiting the site, I noticed several red flags, including an insecure payment gateway.

To further investigate, I performed a series of DNS queries:

- `nslookup xoofi.shop`
- `nslookup -type=NS xoofi.shop`
- Queries against various root DNS servers like `shop.a.root-servers.net` and `xoofi.shop b.gmoregistry.net`, choosing the root DNS server geographically closest to me for better accuracy. 

From these queries, I identified two prominent IP addresses:  
- **37.209.194.4**  
- **82.25.120.19**

I then used `whois` and `nslookup` on these IPs to gather information about their registrants and hosting providers.  

Next, I took screenshots of the site and downloaded the QR code the site urged users to scan. This QR code was analyzed in a sealed, safe environment to check for any embedded malicious code or payloads.

I generated IOC hashes (MD5, SHA1, SHA256) for the QR file, created a detailed forensic report, and contacted the abuse contacts found in the WHOIS records for both the domain and IP ranges.

After reporting, the fraudulent site was shut down by the hosting providers within approximately 10 minutes.

---

_This investigative approach combining OSINT with forensic analysis and rapid escalation is documented throughout this repository._

# Evidence Overview

All crucial visual and technical evidence collected during the **Fake Meesho Scam Investigation** can be found in the [`evidence`](./Evidence) folder.

---

## Included in the Evidence Folder

- **Screenshots** of the fraudulent website, social media lures, and other suspicious activity.  
- **QR Codes** downloaded from the scam site (tested safely in a controlled environment).  
- **Logs and Captures** from DNS and WHOIS queries.  
- **Supporting Files** that document the investigation steps and IOCs.

---

> 📌 Note: The evidence folder contains **all key files needed to validate this investigation** and is intended for forensic review, legal reporting, and brand protection purposes.


## 📌 Summary

- The domain **xoofi.shop** is **fraudulently impersonating Meesho** with infrastructure in both India and Indonesia.  
- The scam involves **social engineering via YouTube, dubious payment flows, and QR code downloads**.  
- DNS, WHOIS, and IP routing all trace back to **well-defined hosts and abuse contacts**.  
- Detailed technical metadata and hashes are included for **forensic review and legal reporting**.  

> ⚠️ All data herein was extracted and validated by a cybersecurity practitioner for **urgent brand protection** and **legal reporting purposes**.

---
