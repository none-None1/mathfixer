# mathfixer, a tool for fixing math in MediaWiki-based wikis
[MediaWiki](https://mediawiki.org)-based wikis usually use Wikipedia to show math.
However, Wikipedia is blocked in some places.

This tool replaces math tags with [MathJax](https://mathjax.org) to let the math be displayed correctly, using a local proxy at 127.0.0.1 (i.e.: this is not a VPN-like tool).

## Installation
mathfixer requires [mitmproxy](https://pypi.org/project/mitmproxy) and [bs4](https://pypi.org/project/bs4). You should set the system proxy IP to be 127.0.0.1 and port to be the port configured for mathfixer for it to work. Also, it requires the command line `mitmdump` (part of mitmproxy) to be in `PATH`.

You can install mathfixer using `pip install mathfixer`.
## Usage
```shell
mathfixer
```
The port `8080` is used for the proxy and the wiki `esolangs.org` is fixed.
```shell
mathfixer -p 1234 -d somewiki.org
```
The port `1234` is used for the proxy and the wiki `somewiki.org` is fixed.

You should bypass the browser cache if you accessed the wiki before.

## Effect
Before: [![2024-09-06-215810.png](https://i.postimg.cc/ydvCHWZ7/2024-09-06-215810.png)](https://postimg.cc/S22vLSdP)

After: [![2024-09-06-215957.png](https://i.postimg.cc/7hY5JQkL/2024-09-06-215957.png)](https://postimg.cc/BLkSdptW)

Note: Both images are screenshots of [https://esolangs.org/wiki/Factorial](https://esolangs.org/wiki/Factorial) which means they are both public domain.
