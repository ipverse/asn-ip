# ipverse-asn-ip

IPv4 and IPv6 subnets (e.g. 100.2.30.0/22) grouped by the announcing autonomous systems. The subnets are aggregated to save space.  

This repository is updated daily.

## Use cases
- Firewalling, e.g. to ban all IP addresses from that notorious, Spam-friendly network provider
- Route advertisment check, see if/how the routes of a specific autonomous system are seen (even over time, thanks to Git's changelog)
- Find out more about a specific ASN (autonomous system number) using the provided lookup table (currently .csv format only) or use it in your own software project for bulk/offline use
- Statistical analysis purposes, e.g. the number of public IPv4 addresses currently announced vs unused/unassigned

## How to use

To download the announced subnets for a specific autonomous system (AS1234 IPv4 adresses in this example), try:  
```$ curl https://raw.githubusercontent.com/ipverse/asn-ip/master/as/1234/ipv4-aggregated.txt```

The same for all IPv6 subnets from AS1234:  
```$ curl https://raw.githubusercontent.com/ipverse/asn-ip/master/as/1234/ipv6-aggregated.txt```

To download the latest lookup table used to enhance the generated route data:  
```$ curl https://raw.githubusercontent.com/ipverse/asn-ip/master/as.csv```

If you plan to use the routing data for firewalling purposes, have a look at:

  - [ipset-blacklistlist](https://github.com/trick77/ipset-blacklist) ipset/iptables based Bash script, IPv4 only
  - [todo](https://localhost) insert link to a popular project with nftables and IPv6 support
