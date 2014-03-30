# grunt-aetheon-cssmin 
> Fork of grunt-contrib-cssmin meant to:

> . Compress CSS files.

> . Combine files via @include

[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donate_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=NYVPSL7GBYD6A&lc=US&item_name=Oscar%20Brito&currency_code=EUR&bn=PP%2dDonationsBF%3abtn_donateCC_LG%2egif%3aNonHosted)

[![Divhide](http://site.divhide.com/assets/img/github_powered_by.jpg)](http://site.divhide.com/) 


## Getting Started
This plugin requires Grunt `~0.4.0`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-contrib-cssmin --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-contrib-cssmin');
```

*This plugin was designed to work with Grunt 0.4.x. If you're still using grunt v0.3.x it's strongly recommended that [you upgrade](http://gruntjs.com/upgrading-from-0.3-to-0.4), but in case you can't please use [v0.3.2](https://github.com/gruntjs/grunt-contrib-cssmin/tree/grunt-0.3-stable).*



## Cssmin task
_Run this task with the `grunt cssmin` command._

### Usage Examples

#### CSS File with @include instructions
```js
cssmin: {
  includeTask: {
    options: {
      // @include instructions will be relative to this path
      relativeTo: "lib/",
    },
    files: {
      'path/to/output.css': ['path/to/include.css']
    }
  }
}
```

The include file may have the following content:

```css


@include("jquery-mobile/jquery-mobile.css");
@include("bootstrap/bootstrap.css");

```

After searching on the _relativeTo_ directory for the including files, will be generated a single file with 
the combined files. Also all the url resources inside the css files will be relative to the value of 
this variable.

#### Other

Check [grunt-contrib-cssmin](https://github.com/gruntjs/grunt-contrib-cssmin) for more usage examples.
