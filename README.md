# chromecast-player-reloaded
[![Donate](https://img.shields.io/badge/Donate-PayPal-blue.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=TFVDFD88KQ322)
[![Donate](https://img.shields.io/badge/Donate-PayPal.Me-lightgrey.svg)](https://www.paypal.me/Rafostar)

### Node chromecast player reloaded.
Based on [xat/chromecast-player](https://github.com/xat/chromecast-player).
Relies on the [castv2-client](https://github.com/thibauts/node-castv2-client) lib
from thibauts.

All credits go to them.<br>
I decided to fork my own version as original project does not seem to be maintained anymore.

### Usage
Start Playback of some video file:

```javascript
const player = require('chromecast-player-reloaded')();
const media = 'http://commondatastorage.googleapis.com/gtv-videos-bucket/ED_1280.mp4';

player.launch(media, (err, p) => {
  p.once('playing', () => {
    console.log('playback has started.');
  });
});
```

Attach to a currently playing session:

```javascript
const player = require('chromecast-player-reloaded')();

player.attach((err, p) => {
  p.pause();
});
```

### Installation

```bash
npm install chromecast-player-reloaded
```

## License
MIT

## Donation
If you like my work please support it by buying me a cup of coffee :grin:

[![PayPal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=TFVDFD88KQ322)
