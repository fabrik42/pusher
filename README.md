## Usage

```javascript

var Pusher = require('pusher');

var pusher = new Pusher({
  appId:  'YOUR_PUSHER_APP_ID',
  appKey: 'YOUR_PUSHER_APP_KEY',
  secret: 'YOUR_PUSHER_SECRET_KEY'
});

var channel = pusher.channel('sync');

channel.trigger('message', function(err, request, response) {
  // do something (this callback is optional)
});

```
Enjoy! :)

## Credits

This lib is based on the work of Dave Hoover aka [redsquirrel](https://github.com/redsquirrel) and his lib [simple_pusher](https://github.com/redsquirrel/simple_pusher).

## License

This code is free to use under the terms of the MIT license.