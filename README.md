torsniff - a sniffer that sniffs torrents from BitTorrent network
======================================


**English** | [简体中文](./README-zh.md)

## Introduction
torsniff is a torrent sniffer, it sniffs torrents that people are using to download movies, music, docs, games and so on from BitTorrent network.

A torrent has valuable information, so you can use torsniff to build your own torrent database(e.g: The Pirate Bay), or to do data mining and analyzing.


## Compiling

> Please ensure you have golang installed in your system environment
```bash
./build.sh
```

## Usage

```
$ ./btsniffer -h

Usage:
  torsniff [flags]

Flags:
  -a, --addr string        listen on given address (default all, ipv4 and ipv6)
  -d, --dir string         the directory to store the torrents (default "$HOME/torrents")
  -h, --help               help for torsniff
  -f, --friends int        max fiends to make with per second (default 500)
  -e, --peers int          max peers to connect to download torrents (default 400)
  -p, --port uint16        listen on given port (default 6881)
  -t, --timeout duration   max time allowed for downloading torrents (default 10s)
  -k, --kwfile string      the keywords file
  -o, --database string    the output database, all torrent will be saved here
  -v, --verbose            run in verbose mode (default true)
```

## Quick start
Use default flags:

`./btsniffer`

## Requirements

* A host having a public IP(recommended), or UDP port forwarding/port mapping in private network/NAT
* Allow UDP traffic get through firewall
* Your ISP/Hosting Provider allows BitTorrent traffic(torsniff works on [vultr.com](https://www.vultr.com/?ref=7114970))

## Protocols
- [DHT Protocol](http://www.bittorrent.org/beps/bep_0005.html)
- [The BitTorrent Protocol Specification](http://www.bittorrent.org/beps/bep_0003.html)
- [BitTorrent  Extension Protocol](http://www.bittorrent.org/beps/bep_0010.html)
- [Extension for Peers to Send Metadata Files](http://www.bittorrent.org/beps/bep_0009.html)

## License
MIT
