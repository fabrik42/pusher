---

# IMPORTANT: This repository is not maintained anymore!

I decided to not maintain this library anymore and instead, work together with @pusher to create a better, actively maintained node.js library for the pusher service. Also, the npm package `pusher` now points to the new repository.
We tried to make the new lib backwards compatible to this, so in best case, your existing apps won't even notice. 

Please move on to https://github.com/pusher/pusher-node-server

---

# Pusher

Pusher is a simple node.js publisher lib for [pusher.com](http://pusher.com/).

## Usage

```javascript

var Pusher = require('pusher');

var pusher = new Pusher({
  appId:  'YOUR_PUSHER_APP_ID',
  appKey: 'YOUR_PUSHER_APP_KEY',
  secret: 'YOUR_PUSHER_SECRET_KEY'
});

var channel = pusher.channel('sync');

var data = { name: "Joe", message_count: 23 };

channel.trigger('message', data, function(err, request, response) {
  // do something (this callback is optional)
});

```
Enjoy! :)

## Credits

This lib is based on the work of Dave Hoover aka [redsquirrel](https://github.com/redsquirrel) and his lib [simple_pusher](https://github.com/redsquirrel/simple_pusher).

## License

This code is free to use under the terms of the MIT license.
