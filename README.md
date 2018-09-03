# GeoJSON Track for HiGlass

> Display your favorite GeoJSON annotation right in HiGlass.

[![HiGlass](https://img.shields.io/badge/higlass-👍-red.svg?colorB=0f5d92)](http://higlass.io)
[![Build Status](https://img.shields.io/travis/flekschas/higlass-geojson/master.svg?colorB=0f5d92)](https://travis-ci.org/flekschas/higlass-geojson)

![HiGlass showing ski areas with Mapbox](/teaser.jpg?raw=true "Ski areas around Park City shown with Mapbox")

**Note**: This is the source code for the GeoJSON track only! You might want to check out the following repositories as well:

- HiGlass viewer: https://github.com/hms-dbmi/higlass
- HiGlass server: https://github.com/hms-dbmi/higlass-server
- HiGlass docker: https://github.com/hms-dbmi/higlass-docker

## Installation

```
npm install higlass-geojson
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
    tilesetUid: 'my-outrageously-fancy-geojson-db',
    uid: 'my-outrageously-fancy-geojson-db',
    type: 'labelled-points-track',
    options: {
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
