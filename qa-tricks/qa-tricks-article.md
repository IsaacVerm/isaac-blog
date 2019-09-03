# QA Tricks

## Grunt

[Grunt](https://gruntjs.com/) is a task runner. A task runner helps with automating your housekeeping jobs:

```
 The less work you have to do when performing repetitive tasks like minification, compilation, unit testing, linting, etc, the easier your job becomes.
```

To use locally installed Grunt (from `package.json`):

```
npx grunt
```

How [Grunt works](https://gruntjs.com/getting-started).

You just need a single file to make it work namely `Gruntfile.js`. The Gruntfile is used to configure and define tasks. It contains the following parts:

* wrapper function
* project and task configuration
* loading plugins and tasks
* custom tasks

Most tasks can be ran in several ways so you need some kind of configuration. This is done with the `grunt.initConfig` function.

To make sure the configuration works the plugin name must be the same as the property name in the `initConfig`:

```
grunt.initConfig({
  uglify: ...
});
```

`uglify` name is `uglify` property in config.

[Plugins](https://github.com/gruntjs) available.

### Use Grunt from within DevTools

DevTools doesn't stand on its own, can be [extended](https://developer.chrome.com/devtools/docs/sample-extensions). You can even make [your own extensions](https://developer.chrome.com/extensions/devtools).

Unfortunately most existing DevTools extensions are quite outdated (e.g. `grunt-devtools` had [latest update](https://github.com/vladikoff/grunt-devtools/commits/master?before=d22425b37b59252bc434c9959ad805602262a404+35) on 3th of February 2014)

Handy because:

```
Grunt DevTools provides a GUI for triggering Grunt tasks. Run tests, build steps, or start up a test server without leaving DevTools.
```

For example you can run API tests relevant to your UI from within DevTools. Can be handy to quickly ascertain if a problem is on the UI side or instead on the API side.
