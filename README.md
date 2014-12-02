# grunt-favicon [![NPM version](https://badge.fury.io/js/grunt-favicon.png)](http://badge.fury.io/js/grunt-favicon) [![Built with Grunt](https://cdn.gruntjs.com/builtwith.png)](http://gruntjs.com/)

[![Npm Downloads](https://nodei.co/npm/grunt-favicon.png?downloads=true&stars=true)](https://www.npmjs.org/package/grunt-favicon)

Generate site favicons via imagick.

# windows not supported !!!

## Options

### options.sizeDepth

### options.colorDepth

### options.fileMode

### options.dirMode

## Examples

``` javascript
grunt.initConfig({
    favicon: {
        // general options
        options: {},
        tasks: {
            // task options
            options: {},
            files: [{
                expand : true,
                cwd    : "src",
                ext    : ".ico",
                dest   : "dest",
                src    : "*.png"
            }]
        }
    }
});
```