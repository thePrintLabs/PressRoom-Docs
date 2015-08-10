> a simple neat theme structured as a boilerplate for [PressRoom](http://press-room.io)    

**Starterr** is built with the support of [Node](http://nodejs.org/), [Bower](http://bower.io/) and [Grunt](http://gruntjs.com/). 

##Quick start

**Starterr** is meant to be used as a strating point to develop your own theme:

1. Download
2. Unzip
3. Rename the unzipped folder and start customizing the `config.xml` file 
4. To edit the **Starterr** source files just open a terminal window at the root folder, and type:

```bash
npm i && bower i
```
Then just start watching:

```bash
grunt watch
```

##Theme file structure:

While developing PressRoom themes you're not bound to a specific directory structure, the only strict requirement is to declare your layout files in `config.xml`

Here we decided to place all of our layout files inside a `layout/` folder. We also opted to create a `components/` folder to hold special fragments and a `partial/` folder to hold fragment commonly shared between files. As said, this act just as an example. 

```bash
├── Gruntfile.js
├── README.md
├── Starterr-logo.png
├── assets
│   ├── bower_components
│   ├── css
│   │   ├── styles.css
│   │   └── toc.css
│   ├── fonts
│   ├── img
│   │   ├── fallback.gif
│   │   └── logo.svg
│   ├── js
│   │   ├── scripts.js
│   │   ├── scripts.min.js
│   │   ├── source
│   │   │   ├── _main__init.js
│   │   │   └── _toc__init.js
│   │   ├── toc.js
│   │   ├── toc.min.js
│   │   └── vendor
│   │       └── modernizr-custom.js
│   ├── pr-manifest.json
│   └── sass
│       ├── base
│       │   ├── _bk-typography.scss
│       │   ├── _breakpoints.scss
│       │   ├── _colors.scss
│       │   ├── _embed.scss
│       │   ├── _fonts.scss
│       │   ├── _globals.scss
│       │   ├── _images.scss
│       │   ├── _logo.scss
│       │   └── _typography.scss
│       ├── components
│       │   ├── _callout.scss
│       │   ├── _cover-image.scss
│       │   ├── _entry-meta.scss
│       │   ├── _gallery.scss
│       │   └── _swiper.scss
│       ├── layout
│       │   ├── _footer.scss
│       │   └── _grid.scss
│       ├── pages
│       │   ├── _all.scss
│       │   ├── _cover.scss
│       │   └── _toc.scss
│       ├── styles.scss
│       ├── themes
│       ├── toc.scss
│       └── utility
├── bower.json
├── config.xml
├── inc
│   ├── functions.php
│   └── pr_scripts.php
├── layouts
│   ├── basic-article.php
│   ├── components
│   │   ├── coverimage.php
│   │   └── fontobserver.php
│   ├── cover.php
│   ├── partials
│   │   ├── content.php
│   │   ├── cover
│   │   │   ├── content.php
│   │   │   └── footer.php
│   │   ├── footer.php
│   │   ├── head.php
│   │   └── header.php
│   └── toc.php
├── package.json
├── screenshot.png
└── version.json
```


##Credits


###Sass

- [Bourbon](https://github.com/thoughtbot/bourbon) *by* [thoughtbot](http://robots.thoughtbot.com/)    
A simple and lightweight mixin library for Sass
- [Scut](http://davidtheclark.github.io/scut/) *by* [David Clark](http://davidtheclark.com/)    
Sass utilities for the frontend laborer
- [Jeet](https://github.com/mojotech/jeet) *by* [MojoTech](http://www.mojotech.com/) 
The most advanced, yet intuitive, grid system available for Sass or Stylus 
- [Mq](https://github.com/guardian/sass-mq) *by the guys at* [The Guardian](http://www.theguardian.com/uk)     
A Sass mixin that helps manipulating media queries in an elegant way 


###Javascript
All the libs here are standalone pure javascript libraries, for maximum performance on mobile and full support for desktop browsers.

- [FluidVids](https://github.com/toddmotto/fluidvids) *by* [Todd Motto](http://toddmotto.com/)   
A lightweight, easy-to-use jQuery plugin for fluid width video embeds. 
- [iDangerous Swiper ](http://www.idangero.us/sliders/swiper/) *by* [iDangero.us](http://www.idangero.us/)  
Mobile touch slider & framework with hardware accelerated transitions
- [FastClick](https://github.com/ftlabs/fastclick) *by the guys at* [FTLabs](http://labs.ft.com/)   
Polyfill to remove click delays on browsers with touch UIs 
