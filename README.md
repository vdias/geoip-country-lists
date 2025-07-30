# GeoIP Country Blocklists

This repository contains daily-updated IPv4 blocklists per country, extracted and derived from MaxMind's GeoLite2 Country database.

## Files

Each `.txt` file contains IPv4 CIDR blocks for the respective country code (ISO 3166-1 alpha-2), one CIDR block per line. These lists are suitable for use in firewall address lists and network filtering tools.

> **Note:** Currently, only the following countries are included in this repository:  
> `CN` (China), `RU` (Russia), `IN` (India), `BR` (Brazil), `VN` (Vietnam), `IR` (Iran), `ID` (Indonesia), and `NG` (Nigeria).

## Use Cases

- MikroTik firewall address-list population
- IPTables, nftables, pf, CrowdSec and other firewall or security tools
- Network access control and geo-based filtering

## Updating

This repository is updated automatically via a scheduled script that downloads the official GeoLite2 CSV files, extracts country IP ranges, and formats them into the `.txt` files you see here.

## License

This repository contains IPv4 blocklists derived from MaxMind’s GeoLite2 Country database.

The GeoLite2 data is provided by MaxMind under the  
[Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).

By using or redistributing this data, you agree to comply with the terms of this license, including:

- Providing proper attribution to MaxMind as the original source of the GeoLite2 data.  
- Sharing any derivative works under the same or a compatible license.  
- Not implying endorsement by MaxMind.

MaxMind and GeoLite2 are trademarks of MaxMind, Inc. This repository is not affiliated with or endorsed by MaxMind.

For full license details and terms, please visit:  
https://dev.maxmind.com/geoip/geolite2-free-geolocation-data

## Attribution

If you use this data in your projects, please include attribution as follows:

> Data derived from MaxMind GeoLite2, available at https://dev.maxmind.com/geoip/geolite2-free-geolocation-data  
> Licensed under Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)  
> https://creativecommons.org/licenses/by-sa/4.0/

## Disclaimer

This data is provided "as-is" without any warranties or guarantees. Use at your own risk.

---

*For questions, contributions, or issues, please open an issue or pull request.*
