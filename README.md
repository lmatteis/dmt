# webtorrent-cli

#### WebTorrent, the streaming torrent client. For the command line.

[![Gitter][webtorrent-cli-gitter-image]][webtorrent-cli-gitter-url]
[![Travis Build][webtorrent-cli-ti]][webtorrent-cli-tu]
[![NPM Version][webtorrent-cli-ni]][webtorrent-cli-nu]
[![NPM Downloads][webtorrent-cli-downloads-image]][webtorrent-cli-downloads-url]

<img src="https://webtorrent.io/img/WebTorrent.png" alt="WebTorrent" width="100">

WebTorrent is the first BitTorrent client that works in the browser, but `webtorrent-cli`,
i.e. *THIS PACKAGE*, is for using WebTorrent from the command line.

`webtorrent-cli` is a simple torrent client for use in node.js, as a command line app. It
uses TCP and UDP to talk to other torrent clients.

**NOTE**: To connect to "web peers" (browsers) in addition to normal BitTorrent peers, use
[`webtorrent-hybrid`](https://github.com/feross/webtorrent-hybrid) which includes WebRTC
support for node.

To use WebTorrent in the browser, see [`webtorrent`](https://github.com/feross/webtorrent).

### Features

- **Use [WebTorrent](https://webtorrent.io) from the command line!**
- **Insanely fast**
- **Pure Javascript** (no native dependencies)
- Streaming
  - Stream to **AirPlay**, **Chromecast**, **VLC player**, and many other devices/players
  - Fetches pieces from the network on-demand so seeking is supported (even before torrent is finished)
  - Seamlessly switches between sequential and rarest-first piece selection strategy
- Supports advanced torrent client features
  - **magnet uri** support via **[ut_metadata](https://github.com/feross/ut_metadata)**
  - **peer discovery** via **[dht](https://github.com/feross/bittorrent-dht)**,
    **[tracker](https://github.com/feross/bittorrent-tracker)**, and
    **[ut_pex](https://github.com/fisch0920/ut_pex)**
  - **[protocol extension api](https://github.com/feross/bittorrent-protocol#extension-api)**
    for adding new extensions

### Install

To install a `webtorrent` command line program, run:

```bash
npm install webtorrent-cli -g
```

### Usage

```bash
$ webtorrent --help
```

To download a torrent:

```bash
$ webtorrent magnet_uri
```

To stream a torrent to a device like **AirPlay** or **Chromecast**, just pass a flag:

```bash
$ webtorrent magnet_uri --airplay
```

There are many supported streaming options:

```bash
--airplay               Apple TV
--chromecast            Chromecast
--mplayer               MPlayer
--mpv                   MPV
--omx [jack]            omx [default: hdmi]
--vlc                   VLC
--xbmc                  XBMC
--stdout                standard out [implies --quiet]
```

In addition to magnet uris, webtorrent supports many ways to specify a torrent:

- magnet uri (string)
- torrent file (buffer)
- info hash (hex string or buffer)
- parsed torrent (from [parse-torrent](https://github.com/feross/parse-torrent))
- http/https url to a torrent file (string)
- filesystem path to a torrent file (string)

[webtorrent-cli]: https://github.com/feross/webtorrent-cli
[webtorrent-cli-gitter-image]: https://img.shields.io/badge/gitter-join%20chat%20%E2%86%92-brightgreen.svg
[webtorrent-cli-gitter-url]: https://gitter.im/feross/webtorrent-cli
[webtorrent-cli-ti]: https://img.shields.io/travis/feross/webtorrent-cli/master.svg
[webtorrent-cli-tu]: https://travis-ci.org/feross/webtorrent-cli
[webtorrent-cli-ni]: https://img.shields.io/npm/v/webtorrent-cli.svg
[webtorrent-cli-nu]: https://www.npmjs.com/package/webtorrent-cli
[webtorrent-cli-downloads-image]: https://img.shields.io/npm/dm/webtorrent-cli.svg
[webtorrent-cli-downloads-url]: https://npmjs.org/package/webtorrent-cli

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](http://standardjs.com)

### License

MIT. Copyright (c) [Feross Aboukhadijeh](http://feross.org).
