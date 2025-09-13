# FAKE MESHO SCAM – Technical Summary

This repo documents the forensic investigation and IoCs tied to the "Fake Mesho" scam, targeting Meesho's brand via fraudulent websites and social engineering.

## Indicators of Compromise (IOC)

- **Suspicious YouTube:**  
  - www.youtube.com/@Meeshosalesoffer (used for victim luring) [attached_file:1][attached_file:5]

- **Fraudulent Sites:**  
  - Redirect:  
    - https://www.googleadservices.com/pagead/aclk?...  
  - Main fake site:  
    - https://xoofi.shop [attached_file:1][attached_file:5]

## DNS & IP Details

- **Nameservers:**  
  - ns1.dns-parking.com  
  - ns2.dns-parking.com  
- **IP Addresses:**  
  - 37.209.194.4 (Indonesia - Telkomsel)  
  - 82.25.120.19 (Mumbai - Hostinger) [attached_file:1][attached_file:4][attached_file:5]

## Domain Info

- Registrar: Hostinger Operations, UAB
- WHOIS Server: whois.hostinger.com
- Abuse Contact: abuse@hostinger.com
- Created: 2025-09-01
- Expires: 2026-09-01
- Registrant Country: US
- DNSSEC: Unsigned [attached_file:4][attached_file:5]

## QR Code Sample

- **Hashes (file tested, not malicious):**
  - MD5: `4aa5e4adfd97444acba19f53b1180da9`
  - SHA256: `49be5659d85383797f1ff4017e39c916111d63d2c11129f6c79b68c9feaffefe`
  - SHA1: `35f872c3653d1002a9e39eabdff881fc7beca03` [attached_file:4][attached_file:5]

## IP Attribution

- **37.209.194.4**: Telkomsel, Jakarta, Indonesia [attached_file:4][attached_file:5]
- **82.25.120.19**: Hostinger, Mumbai, India [attached_file:4][attached_file:5]

---

## Summary

Infrastructure leverages false branding, cross-border hosting, and social engineering.  
Full technical metadata, hashes, and abuse contacts included for incident response. [attached_file:5]


