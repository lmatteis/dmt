This is a reference implementation for the Decentralized Mutable Torrents extension proposed here: https://github.com/lmatteis/bittorrent.org/blob/master/beps/bep_0046.rst

Follow discussion about this BEP here: https://github.com/bittorrent/bittorrent.org/issues/34

### Install

```bash
npm install
```

### Usage

```bash
$ ./bin/cmd.js --help

- mutable torrents commands:
  keypair                                         Create new public-private keypair
  publish <public-key> <private-key> <info-hash>  Publish new torrent
  consume <public-key>                            Downloads mutable torrent
```

### License

MIT.
