# Labelled Points Track for HiGlass

> Explore datasets containing millions of points with labels in HiGlass

[![HiGlass](https://img.shields.io/badge/higlass-👍-red.svg?colorB=0f5d92)](http://higlass.io)
[![Build Status](https://img.shields.io/travis/pkerpedjiev/higlass-labelled-points-track/master.svg?colorB=0f5d92)](https://travis-ci.org/pkerpedjiev/higlass-labelled-points-track)

![A view of over 1 million data points, heavily downsampled](/teaser.png?raw=true "A downsampling of many points")

**Note**: This is the source code for the labelled points track only! You might want to check out the following repositories as well:

- HiGlass labelled points track (this repository): https://github.com/higlass/higlass-labelled-points-tracks
- HiGlass viewer: https://github.com/higlass/higlass
- HiGlass server: https://github.com/higlass/higlass-server
- HiGlass docker: https://github.com/higlass/higlass-docker

## Installation

```
npm install higlass-labelled-points-track
```

## Usage

To try this track out, head over to https://github.com/pkerpedjiev/million-primes
and start a server using the provided notebook.

1. Make sure you load this track prior to `hglib.js`. For example:

```
<script src="higlass-labelled-points-track.js"></script>
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
    type: 'labelled-points-track',
    options: {
        labelField: 'label',
        xPosField: 'x',
        yPosField: 'y'
    },
  },
  ...
}
```

Take a look at [`src/index.html`](src/index.html) for an example.

## Development

### Installation

```bash
$ git clone https://github.com/pkerpedjiev/labelled-points-track && higlass-labelled-points-track
$ npm install
```

### Commands

**Developmental server**: `npm start`
**Production build**: `npm run build`
