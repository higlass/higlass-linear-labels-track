# Linear Labels Track

> Tile-based labels along a 1D axis (x- or y-)

[![HiGlass](https://img.shields.io/badge/higlass-👍-red.svg?colorB=0f5d92)](http://higlass.io)
[![Build Status](https://img.shields.io/travis/higlass/higlass-linear-labels-track/master.svg?colorB=0f5d92)](https://travis-ci.org/higlass/higlass-linear-labels-track)

<img src="/teaser.png?raw=true" width="600" />

**Note**: This is the source code for the linear labels track only! You might want to check out the following repositories as well:

- HiGlass linear labels track (this repository): https://github.com/higlass/higlass-linear-labels-tracks
- HiGlass viewer: https://github.com/higlass/higlass
- HiGlass server: https://github.com/higlass/higlass-server
- HiGlass docker: https://github.com/higlass/higlass-docker

## Installation

```
npm install higlass-linear-labels-track
```

## Usage

### Server

First, make sure that you have a server capable of serving tiled labels.
[This notebook](https://github.com/higlass/higlass-python/blob/pkerpedjiev/merge-branches/notebooks/Label%20server%20example.ipynb) provides a functioning demo
server that can be run locally. In the last cell, a viewconf is provided which
can be used to instantiate HiGlass (see step 2 below).

### Client

1. Make sure you load this track prior to `hglib.js`. For example:

```
<script src="higlass-linear-labels-track.js"></script>
<script src="hglib.js"></script>
<script>
  ...
</script>
```

2. Now, configure the track in your view config and be happy! 

```
{
  ...
  {
    server: 'http://localhost:8001/api/v1',
    tilesetUid: 'blah',
    type: 'linear-labels-track',
    options: {
        labelField: 'label',
        xPosField: 'x',
    },
  },
  ...
}
```

Take a look at [`src/index.html`](src/index.html) for an example.

## Development

### Installation

```bash
$ git clone https://github.com/higlass/linear-labels-track && higlass-linear-labels-track
$ npm install
```

### Commands

**Developmental server**: `npm start`
**Production build**: `npm run build`
