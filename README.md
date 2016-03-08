# Osram lightify for Node.js

Low-level client library for controlling Zigbee lights, switches by Lightify Wireless gateway
[Amazon link of OSRAM Lightify Wiress Gateway] (http://www.amazon.com/LIGHTIFY-wireless-connected-lighting-technology/dp/B00R1PB2T0)
[![Npm](https://img.shields.io/npm/v/node-lightify.svg)](http://npmjs.com/package/node-lightify)

## This project is under development. all features might change


## Install

```bash
$ npm install node-lightify
```

## Usage

```javascript
var lightify = require('lightify');

lightify.start('x.x.x.x').then(function(data){
    return lightify.discovery();
}).then(function(data) {
    console.log(data.result)
}
```

## API
* start
  + connect to lightify gateway using tcp port 4000
* discovery
  + discover Zigbee devices connected to the gateway
* zone_discovery
  + discover zones defined on the gateway
* node_on_off
  + turn light on or off
* node_brightness
  + adjust light brightness
* node_temperature
  + adjust light temperature
* node_color
  + change light color


## Contributing

Contributions are very welcome! Please note that by submitting a pull request for this project, you agree to license your contribution under the [MIT License](https://github.com/rainlake/node-lightify/blob/master/LICENSE) to this project.

## License

Published under the [MIT License](https://github.com/rainlake/node-lightify/blob/master/LICENSE).