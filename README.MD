# Docker xmrig

Run `meta-miner` using Docker.

This image uses `https://github.com/MoneroOcean/meta-miner` (and `https://github.com/xmrig/xmrig/`)

## Usage

Append any `mm.js` params after the image name. i.e:

```shell
docker run -it --rm lchaia/meta-miner --pass=WORKDER_ID:EMAIL --user=XMR_WALLET --miner="xmrig -o 127.0.0.1:3333 -t 0 --donate-level 0 --cpu-priority 5" --pool=gulf.moneroocean.stream:10001
```

## Docker Compose example

```yaml
version: "3"

services:
  xmrig:
    image: lchaia/meta-miner
    build:
      context: ./src
    command: --pass=WORKDER_ID:EMAIL --user=XMR_WALLET --miner="xmrig -o 127.0.0.1:3333 -t 0 --donate-level 0 --cpu-priority 5" --pool=gulf.moneroocean.stream:10001
```

## Copyrights

Code from this repository is released under MIT license.
xmrig code is released under GPL-3

## Donations

Please consider [donating to the xmrig team](https://github.com/xmrig/xmrig#donations)
and to the [meta miner team](https://github.com/MoneroOcean/meta-miner#developer-donations)
