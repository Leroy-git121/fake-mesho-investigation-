# FAKE MESHO Scam — Full Forensic Technical Report

---

## Investigation Overview

This report describes IoCs, technical infrastructure, and social methods behind a scam imitating Meesho.  
Data sourced from DNS records, WHOIS, geo-IP analysis, HTML forensics, and malware testing. 

---

## Main Indicators of Compromise (IOC)

- **YouTube Channel:**  
  - www.youtube.com/@Meeshosalesoffer (for redirection/social engineering) 
- **Fake Sites:**  
  - Google Ads redirect  
  - Primary: https://xoofi.shop
  - Site design mimics legitimate Meesho offers 

---

## Domain, DNS, and WHOIS Analysis

| Attribute       | Value                    |
|-----------------|-------------------------|
| Domain Name     | xoofi.shop              |
| Registrar       | Hostinger Ops, UAB      |
| WHOIS Server    | whois.hostinger.com     |
| Abuse Contact   | abuse@hostinger.com     |
| Created         | 2025-09-01              |
| Expires         | 2026-09-01              |
| Status          | clientTransferProhibited, addPeriod |
| DNSSEC          | Unsigned                |
| Registrant Ctry | US                      |
| Nameservers     | ns1/2.dns-parking.com   |
| Main IPs        | 37.209.194.4, 82.25.120.19 |

---

## IP Attribution & Routing

### 37.209.194.4 — Indonesia (Telkomsel)

- Netname: TELKOMSELNET-ID
- Provider: PT.TELKOMSEL Indonesia
- Abuse: hostmaster@telkomsel.co.id
- Route: 39.209.0.0/16 (AS23693, Jakarta)
- Status: Allocated Portable
- Address: Telkom Landmark Tower, Jakarta, Indonesia

### 82.25.120.19 — Mumbai, India (Hostinger)

- Netname: HOSTINGER-HOSTING
- Geolocation: Mumbai, Maharashtra (19.076090, 72.877426)
- Organization: Private Customer (Cyprus)
- Abuse: report@abuseradar.com
- Route: 82.25.120.0/21 (AS47583, HOSTINGER IN)
- Status: Assigned PA

---

## QR Code Forensics

Site prompts for QR code download as part of misleading purchase flow.  
Hashes (confirmed safe in lab):

- **MD5:** `4aa5e4adfd97444acba19f53b1180da9`
- **SHA256:** `49be5659d85383797f1ff4017e39c916111d63d2c11129f6c79b68c9feaffefe`
- **SHA1:** `35f872c3653d1002a9e39eabdff881fc7beca03`

---

## Infrastructure Insights

- Multi-region hosting in Indonesia and India.
- Nameservers use DNS-parking for anonymity/quick changes.
- WHOIS and registrar conceal registrant details.
- DNS, WHOIS, and IP attribution all link to traceable hosts and abuse contacts.
- Full technical details for takedown and forensic analysis.

---

## Social Engineering & Attack Narrative

- YouTube/social media used for victim luring.
- Fake e-commerce site uses Meesho branding, “Free” offers, and urgent payment prompts.
- Payment flow ambiguous; potential for fraud.
- QR codes used for social baiting. File tested clean but could be swapped.

---

## Brand Protection & Incident Response

- Block/monitor the DNS/IPs listed.
- Report fraudulent behavior to Hostinger and Telkomsel using provided contacts.
- Abuse and technical details are validated for urgent brand protection and legal escalation.

---


Report compiled September 2025 from validated sources and independent forensic testing. Suitable for incident response, takedown, and audit.
