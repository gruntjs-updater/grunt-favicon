# grunt-favicon [![NPM version](https://badge.fury.io/js/grunt-favicon.png)](http://badge.fury.io/js/grunt-favicon) [![Built with Grunt](https://cdn.gruntjs.com/builtwith.png)](http://gruntjs.com/)

[![Npm Downloads](https://nodei.co/npm/grunt-favicon.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.org/package/grunt-favicon)
[![Npm Downloads](https://nodei.co/npm-dl/grunt-favicon.png?height=3&months=3)](https://www.npmjs.org/package/grunt-favicon)

Generate site favicons via [ImageMagick](http://www.imagemagick.org/).

**WARNING:** This extension require global install ImageMagick.
* For Windows go to the [ImageMagick](http://www.imagemagick.org/) and download installer.
* For Debian, Ubuntu or Mint run on command line: sudo apt-get install imagemagick
* For Redhut, Centos or Fedora run on command line: sudo yum install ImageMagick
* For Gentoo run on command line: sudo emerge media-gfx/imagemagick
* For MacOS run on command line: sudo port install ImageMagick

## Options

### options.countOfImages

* **type** &lt;number&gt;
* **default** 6

Count of images into icon.

### options.colorDepth

* **type** &lt;number&gt;
* **default** 8

Count of bits for color.

## Example

``` javascript
grunt.initConfig({
    favicon: {
        options: {
            // Icons contains 3 images
            // (16x16, 32x32, 48x48)
            countOfImages: 3,
            // for 256 colors, is max value
            colorDepth: 8
        },
        tasks: {
            options: {
                // override options if needed
            },
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