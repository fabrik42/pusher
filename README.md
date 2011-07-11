# Pusher

Pusher is a simple node.js publisher lib for [pusher.com](http://pusher.com/).

## Installation

Pusher is [available on npm](http://search.npmjs.org/#/pusher).

```
$ npm install pusher
```

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