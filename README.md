# baseview

`baseview` is a minimalistic CouchBase client for node.js based on the minimalistic CouchDB driver `nano`[1]

# usage

``` js
  baseview = require('baseview')('http://127.0.0.1:8092')

  ...

  baseview.view('design_doc', 'view_name', function(error, data) {
    console.log(error, data);
  });
```



# contribute

everyone is welcome to contribute. patches, tests, bugfixes, new features

1. create an [issue][2] on github so the community can comment on your idea
2. fork `baseview` in github
3. create a new branch `git checkout -b my_branch`
4. create tests for the changes you made
5. make sure you pass both existing and newly inserted tests
6. commit your changes
7. push to your branch `git push origin my_branch`
8. create an pull request

[1]: https://github.com/dscape/nano
[2]: http://github.com/Presive/baseview/issues