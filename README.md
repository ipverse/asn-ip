# ipverse-announced-routes

A collection of IPv4 and IPv6 routes grouped by the announcing autonomous systems. The routes are aggregated to save space.  
This repository is updated daily.

## Potential Use cases
- Firewalling, e.g. to ban all IP addresses from that annoying, Spam-friendly network provider
- Route advertisment check, see if/how the routes of a specific autonomous system are seen (even over time, thanks to git's changelog)
- Statistical analysis purposes, e.g. the number of public IPv4 addresses currently announced vs unused/unassigned
- Find out more about a specific ASN using the provided lookup table (currently .csv format only) or use it in your own software project for offline use

## How to use

Most likely, you won't need to clone the repository. To download the announced routes for a specific autonomous system (AS1234 IPv4 adresses in this example), try:  
```$ curl https://raw.githubusercontent.com/ipverse/announced-routes/master/as/1234/ipv4-aggregated.txt```

The same for all IPv6 routes for AS1234:  
```$ curl https://raw.githubusercontent.com/ipverse/announced-routes/master/as/1234/ipv6-aggregated.txt```

To download the latest lookup table used to enhance the generated route data:  
```$ curl https://raw.githubusercontent.com/ipverse/announced-routes/master/as.csv```

If you plan to use the routing data for firewalling purposes, have a look at:

  - [ipset-blacklistlist](https://github.com/trick77/ipset-blacklist) ipset/iptables based Bash script, IPv4 only
  - [todo](https://localhost) insert link to a popular project with nftables and IPv6 support
