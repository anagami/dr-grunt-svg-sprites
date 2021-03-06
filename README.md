# dr-grunt-svg-sprites

> Grunt plugin to create SVG sprites with PNG fallbacks at needed sizes

## Getting Started
This plugin requires Grunt `~0.4.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install dr-grunt-svg-sprites --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('dr-grunt-svg-sprites');
```

## The "svg_sprites" task

### Overview
In your project's Gruntfile, add a section named `svg_sprites` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  svg_sprites: {
    options: {
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    },
  },
})
```

### Options


#### options.paths
Type: `Object`

##### options.paths.elements
Type: `String`

Optional. Source path of svg elements to composite sprite-elements.


##### options.paths.spriteElements
Type: `String`
Source path of the svg elements to make up a sprite.

##### options.paths.sprites
Type: `String`

Destination path of the generated sprite images.

##### options.paths.css
Type: `String`

Destination path of the generated stylesheet.
      
#### options.map
Type: `Object`



#### options.prefix
Type: `String`
Default value: `''`

Optional. Stylesheet

#### options.cssSuffix
Type: `String`
Default value: `'css'`

Optional. Stylesheet filetype suffix. 

#### options.unit
Type: `Number`

Defines unit size of the grid the sprite elements snap to.

#### options.refSize
Type: `String`

Defines the default size

#### options.sizes
Type: `Object`

A hash of size labels and values (`Number`).
        
#### options.sprites
Type: `Object`


{spriteName}


### Usage Examples

#### Default Options

```js
grunt.initConfig({
  svg_sprites: {
    paths: {
      spriteElements: "img/_source/svg-logos",
      sprites: "img/_source/sprites",
      css: "css/shared",
    },
  },
})
```

#### Custom Options

```js
grunt.initConfig({
  svg_sprites: {
    paths: {
      elements: "img/_source/svg-logo-elements",
      spriteElements: "img/_source/svg-logos",
      sprites: "img/_source/sprites",
      css: "css/shared",
    },
  },
})
```
