# grunt-minify-html [![Build Status](https://travis-ci.org/sindresorhus/grunt-minify-html.svg?branch=master)](https://travis-ci.org/sindresorhus/grunt-minify-html)

> Minify HTML using [minimize](https://github.com/Moveo/minimize)

*Issues with the output should be reported on the minimize [issue tracker](https://github.com/Moveo/minimize/issues).*

The differs from [grunt-contrib-htmlmin](https://github.com/gruntjs/grunt-contrib-htmlmin) in that it uses a [HTML-parser](https://github.com/Moveo/minimize#credits) instead of a [bunch of fragile regexes](https://github.com/kangax/html-minifier/blob/27fce5b5a7c166ea6149fba78a418e475658f075/src/htmlparser.js#L35-L41).


## Install

```sh
$ npm install --save-dev grunt-minify-html
```


## Usage

```js
grunt.initConfig({
	minifyHtml: {										// task
		options: {										// dictionary of options
			cdata: true
		},
		dist: {											// target
			files: {									// dictionary of files
				'dist/index.html': 'src/index.html'		// 'destination': 'source'
			}
		}
	}
});

grunt.loadNpmTasks('grunt-minify-html');
grunt.registerTask('default', ['minifyHtml']);
```


## Options

See the minimize [options](https://github.com/Moveo/minimize#options).


## License

MIT © [Sindre Sorhus](http://sindresorhus.com)
