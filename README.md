# NuoDB    - node.js

[![Build Status](https://travis-ci.org/nuodb/node-db-nuodb.png?branch=master)](https://travis-ci.org/nuodb/node-db-nuodb)

This module builds a native [Google V8](https://developers.google.com/v8/) C++ binding to let you easily integrate your [node.js](http://www.nodejs.org) web applications with [NuoDB](http://www.nuodb.com).

### Requirements
`make`  
`g++`

### Install

    $ npm install db-nuodb

### Example

```javascript
var nuodb = require('db-nuodb');
new nuodb.Database({
    hostname: 'localhost',
    user: 'dba',
    password: 'goalie',
    database: 'test',
    schema: 'hockey'
}).on('error', function(error) {
    console.log('ERROR: ' + error);
}).on('ready', function(server) {
    console.log('Connected to ' + server.hostname + ' (' + server.version + ')');
}).connect();
```

### License

[NuoDB License](https://github.com/nuodb/nuodb-drivers/blob/master/LICENSE)

[![githalytics.com alpha](https://cruel-carlota.pagodabox.com/1f9431fe8d36367b37644bd77eb55724 "githalytics.com")](http://githalytics.com/nuodb/node-db-nuodb)
