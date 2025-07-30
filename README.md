# GeoIP Country Blocklists

This repository contains daily-updated IPv4 blocklists per country, extracted and derived from MaxMind's GeoLite2 Country database.

It also includes an additional blocklist (`IPsum-Level4`) generated from the IPsum project, containing IP addresses associated with suspicious or malicious behavior.

## Files

Each `.txt` file contains IPv4 CIDR blocks for the respective country code (ISO 3166-1 alpha-2), one CIDR block per line. These lists are suitable for use in firewall address lists and network filtering tools.

The IPsum-level list is stored as a MikroTik-compatible script under:

- `MK/IPsum-Level4.rsc` — containing `/ip firewall address-list` commands for MikroTik
- Uses the address list name `IPsum-Level4` inside the firewall rule set

> **Note:** Currently, only the following countries are included from MaxMind GeoLite2:  
> `CN` (China), `RU` (Russia), `IN` (India), `BR` (Brazil), `VN` (Vietnam), `IR` (Iran), `ID` (Indonesia), and `NG` (Nigeria).

## Use Cases

- MikroTik firewall address-list population
- IPTables, nftables, pf, CrowdSec and other firewall or security tools
- Network access control and geo-based filtering
- Supplementary IP threat intelligence via IPsum-Level4

## Updating

This repository is updated automatically via scheduled scripts:

- The GeoLite2 blocklists are generated from the official MaxMind GeoLite2 CSV files, extracting IPv4 ranges per country.
- The IPsum-Level4 blocklist is fetched from the IPsum project (level 4), converted into MikroTik RSC format, and committed if changed.

## Sources & License

### MaxMind GeoLite2

The GeoLite2 data is provided by MaxMind under the  
[Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).

By using or redistributing this data, you agree to comply with the terms of this license, including:

- Providing proper attribution to MaxMind as the original source  
- Sharing any derivative works under the same or compatible license  
- Not implying endorsement by MaxMind

Full license details:  
https://dev.maxmind.com/geoip/geolite2-free-geolocation-data

### IPsum

The IPsum-Level4 list is sourced from the [IPsum project by @stamparm](https://github.com/stamparm/ipsum).

- Source URL: https://raw.githubusercontent.com/stamparm/ipsum/refs/heads/master/levels/4.txt
- Level 4 includes IP addresses observed in abuse events (e.g. scanning, brute-force, botnets)
- The data is collected and maintained by the IPsum project; usage subject to their terms

## Attribution

If you use this data in your projects, please include attribution as follows:

> Country IP data derived from MaxMind GeoLite2, available at https://dev.maxmind.com/geoip/geolite2-free-geolocation-data  
> Licensed under Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)  
> https://creativecommons.org/licenses/by-sa/4.0/

> IP-level threat intelligence derived from the IPsum project  
> https://github.com/stamparm/ipsum

## Disclaimer

This data is provided "as-is" without any warranties or guarantees. Use at your own risk.

---

*For questions, contributions, or issues, please open an issue or pull request.*
