# GeoIP Country Blocklists

This repository contains daily-updated IPv4 blocklists per country, extracted from MaxMind's GeoLite2 Country database.

## Files

Each `*.txt` file contains IPv4 CIDR blocks for the respective country code (ISO 3166-1 alpha-2), one per line.

Example:
CN.txt # China
RU.txt # Russia

## License

- MaxMind GeoLite2 © MaxMind, used under license.
- This repo contains only **derived data** for firewall use.

See https://dev.maxmind.com/geoip/geolite2-free-geolocation-data for licensing.

## Updating

This repository is updated automatically via a scheduled script using official CSV files.

## Use Cases

- MikroTik `address-list` population
- IPTables, nftables, pf, CrowdSec, etc.
