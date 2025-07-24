# Snap Peek
Directly access ETH transactions/blocks via Erigon snap sync torrents

### The Idea
Sometimes you want to quickly analyze ETH transactions in a certain block range.  
To do this you either have to run a own node (archive node for older blocks) or rent RPC access to someone elses Node.  

Luckily Erigon Snap Sync works via normal BitTorrent or Webseeds (HTTP R2 S3 Fallback Server).  
We are going to develop a little (go) lib that wraps erigon-lib to download .seg/.idx files and parses them without running a real ETH Node.

### TODO:
- [ ] Parse [manifest.txt](https://erigon31-v1-snapshots-mainnet.erigon.network/manifest.txt)
- [ ] Implement BitTorrent downloader (probably wrap erigon-lib/erigon-db)
- [ ] Use Erigon's decompressor to unpack .seg/.idx files
- [ ] Parse RLP encoded TXs to usable format
