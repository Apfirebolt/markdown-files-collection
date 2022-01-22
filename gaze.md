# gaze [![Build Status](http://img.shields.io/travis/shama/gaze.svg)](https://travis-ci.org/shama/gaze) [![Build status](https://ci.appveyor.com/api/projects/status/vtx65w9eg511tgo4)](https://ci.appveyor.com/project/shama/gaze)

A globbing `fs.watch` wrapper built from the best parts of other fine watch libs.  
Compatible with Node.js >= 4.x, Windows, macOS, and Linux.

![gaze](http://dontkry.com/images/repos/gaze.png)

[![NPM](https://nodei.co/npm/gaze.png?downloads=true)](https://nodei.co/npm/gaze/)

## Usage
Install the module with: `npm install gaze` or place into your `package.json`
and run `npm install`.

const gaze = require('gaze');


### Alternate Interface

```javascript
const {Gaze} = require('gaze');

const gaze = new Gaze('**/*');

// Files have all started watching
gaze.on('ready', watcher => { });

// A file has been added/changed/deleted has occurred
gaze.on('all', (event, filepath) => { });
```

### Errors

```javascript
gaze('**/*', (error, watcher) => {
  if (error) {
    // Handle error if it occurred while starting up
  }
});

// Or with the alternative interface
const gaze = new Gaze();
gaze.on('error', error => {
  // Handle error here
});
gaze.add('**/*');
```

### Minimatch / Glob

See [isaacs's `minimatch`](https://github.com/isaacs/minimatch) for more
information on glob patterns.

## Documentation

### gaze([patterns, options, callback])

* `patterns` {`String`|`Array`} File patterns to be matched
* `options` {`Object`}
* `callback` {`Function`}
  * `err` {`Error` | `null`}
  * `watcher` {`Object`} Instance of the `Gaze` watcher

### Class: `gaze.Gaze`

Create a `Gaze` object by instancing the `gaze.Gaze` class.

```javascript
const Gaze = require('gaze').Gaze;
const gaze = new Gaze(pattern, options, callback);
```

#### Events

* `added(filepath)` When a file has been added to a watch directory.
* `end()` When the watcher is closed and watches have been removed.
* `error(err)` When an error occurs.
* `nomatch` When no files have been matched.

## Similar Projects

Other great watch libraries to try are:

* [paulmillr's `chokidar`](https://github.com/paulmillr/chokidar)
* [amasad's `sane`](https://github.com/amasad/sane)
* [mikeal's `watch`](https://github.com/mikeal/watch)

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style.
Add unit tests for any new or changed functionality. Lint and test your code
using [grunt](http://gruntjs.com/).

## Release History
* 1.1.3 - Fix for Node 10 support (@aredridel). Officially dropping support for Node < 4.
* 1.1.2 - Prevent more `ENOENT` errors from escaping (@alexgorbatchev).
* 1.1.1 - Prevent `fs.watch` errors from escaping error handler (@rosen-vladimirov). Fix `_addToWatched` without `path.sep` (@wyicwx).


## License
Copyright (c) 2018 Kyle Robinson Young  
Licensed under the MIT license.