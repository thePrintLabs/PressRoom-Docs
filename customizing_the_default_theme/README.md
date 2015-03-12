# Customizing the Starterr theme

The **Starterr** theme has been built with the support of [Node](http://nodejs.org/), [Bower](http://bower.io/) and [Grunt](http://gruntjs.com/).

###Quick start

To edit its source files just open a terminal window at the theme root folder, and type:

```bash
npm i && bower i
```
Then just start watching:

```bash
grunt watch
```

###Basic theme file structure:

```bash
|____starterr
| |____.bowerrc
| |____.editorconfig
| |____.gitignore
| |____.jshintrc
| |____assets
| | |____bower_components
| | |____css
| | | |____styles.a38a4712.css
| | | |____toc.7a77eb84.css
| | |____fonts
| | |____img
| | | |____fallback.gif
| | |____js
| | | |____scripts.min.665cf2e5.js
| | | |____source
| | | | |_____main__init.js
| | | | |_____toc__init.js
| | | |____toc.min.5b460967.js
| | |____sass
| | | |____base
| | | | |_____breakpoints.scss
| | | | |_____colors.scss
| | | | |_____embed.scss
| | | | |_____fonts.scss
| | | | |_____globals.scss
| | | | |_____images.scss
| | | | |_____typography.scss
| | | |____components
| | | | |_____callout.scss
| | | | |_____cover-image.scss
| | | | |_____entry-meta.scss
| | | | |_____swiper.scss
| | | |____layout
| | | | |_____grid.scss
| | | |____pages
| | | | |_____all.scss
| | | | |_____toc.scss
| | | |____styles.scss
| | | |____toc.scss
| | | |____utility
| |____bower.json
| |____Gruntfile.js
| |____inc
| | |____functions.php
| |____layouts
| | |____basic-article.php
| | |____components
| | | |____coverimage.php
| | |____index.php
| | |____partials
| | | |____content.php
| | | |____head.php
| | |____toc.php
| |____package.json
| |____version.json
```

##Credits


###Sass
Bourbon and Scut together may seems an overload but since they are mixing libraries you'll generate just from what you'll use ; )

- [Bourbon](https://github.com/thoughtbot/bourbon) *by* [thoughtbot](http://robots.thoughtbot.com/)
A simple and lightweight mixin library for Sass
- [Scut](http://davidtheclark.github.io/scut/) *by* [David Clark](http://davidtheclark.com/)
Sass utilities for the frontend laborer
- [Jeet](https://github.com/mojotech/jeet) *by* [MojoTech](http://www.mojotech.com/)
The most advanced, yet intuitive, grid system available for Sass or Stylus
- [Mq](https://github.com/guardian/sass-mq) *by the guys at* [The Guardian](http://www.theguardian.com/uk)
A Sass mixin that helps manipulating media queries in an elegant way
- [Knife](http://pushplaybang.github.io/knife/) by [Paul van Zyl](http://nonacreative.com/)
Nail vertical rhythm, modular scale, and REMs like a boss with this simple set of SASS/SCSS variables, functions and mixins.


###Javascript
All the libs here are standalone pure javascript libraries, for maximum performance on mobile and full support for desktop browsers.

- [textFit](https://github.com/STRML/textFit) *by* Samuel Reed
A jQuery-free component that quickly fits single and multi-line text to the width (and optionally height) of its container.
- [FluidVids](https://github.com/toddmotto/fluidvids) *by* [Todd Motto](http://toddmotto.com/)
A lightweight, easy-to-use jQuery plugin for fluid width video embeds.
- [iDangerous Swiper ](http://www.idangero.us/sliders/swiper/) *by* [iDangero.us](http://www.idangero.us/)
Mobile touch slider & framework with hardware accelerated transitions
- [FastClick](https://github.com/ftlabs/fastclick) *by the guys at* [FTLabs](http://labs.ft.com/)
Polyfill to remove click delays on browsers with touch UIs


