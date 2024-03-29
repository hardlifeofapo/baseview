# baseview

`baseview` is a minimalistic CouchBase client for node.js based on the minimalistic CouchDB driver [nano][1].

CouchBase provides view data as JSON, which can be accessed and streamed with this client. To store and retrieve single documents/key-value pairs, the [memcached][2]-library is required.

# usage

``` js
  baseview = require('baseview')('http://127.0.0.1:8092')

  ...

  baseview.view('design_doc', 'view_name', function(error, data) {
    console.log(error, data);
  });
```

## example with socket.io
````js
  io.sockets.on('connection', function (socket) {
    baseview.view('feed', 'images', function(error, data) {
      socket.emit('image_feed', data.rows);
    });
  });
````


# contribute

everyone is welcome to contribute. patches, tests, bugfixes, new features

1. create an [issue][3] on github so the community can comment on your idea
2. fork `baseview` in github
3. create a new branch `git checkout -b my_branch`
4. create tests for the changes you made
5. make sure you pass both existing and newly inserted tests
6. commit your changes
7. push to your branch `git push origin my_branch`
8. create an pull request

# meta

proudly presented by [presive][4], Barcelona.

[1]: https://github.com/dscape/nano
[2]: https://github.com/elbart/node-memcache
[3]: http://github.com/Presive/baseview/issues
[4]: http://www.presive.com