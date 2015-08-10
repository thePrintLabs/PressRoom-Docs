# Theming

In **PressRoom** you are able to set custom themes for each *Editorial Project*. This setting could be overwritten per each *Edition* in the **Edition Meta** tab.

Developing **PressRoom** themes is quick and easy since they inherits almost the same logic used for [Wordpress Theme Development ](http://codex.wordpress.org/Theme_Development/ "Wordpress Theme Devepopment")

##File Structure

**PressRoom** themes resides inside the ```/pressroom/themes/``` folder.

Themes are essentially made of a config.xml file and a set of **layout files** and assets (css, js, fonts, images, etc. ). Everything has been built for maximum flexibility, thus you are not forced to follow a specific folder structure to organize this contents.


### functions.php
Each **PressRoom** theme could use his own `functions.php` file. Place it wherever make sense for you, it will be recognized automatically.

###config.xml

Defines Theme's metadata,layouts path and behaviour (rules).

####Theme Metadata

- __uniqueid__ _You awesome theme name namespace (lowercase)_ (required)
- __name__  _Theme name_ (required)
- __date__ _Theme creation date_ (required)
- __version__ _Semantic versioning_ (http://semver.org/) (required)
- __description__ _Theme description_ (optional)
- __thumbnail__ _Theme thumbnail_ (required)
- __website__ _Theme URI_ (optional)
- __author__ _Theme Author_ (optional)
  + __name__ _Author fullname_ (optional)
  + __email__ _Author email_ (optional)

- __layouts__ wrap a list of layouts
- __item__ a single layout
    + __name__ _layout name. It'll be shown in the_ __flatplan__ (required)
    + __rule__ _There are two kind of rules:_ 
        + __content__ _A layout file used to render content items (post, pages, custom post types)_
        + __toc__ _A layout files used to render the Table of Contents_ (required)
    + __description__ _A comment describing the layout unique features_ (optional) 
    + __path__ _Layout file path. Can be anything below the theme folder_ (required)

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<theme>
    <uniqueid>starterr</uniqueid>
    <name>Starterr</name>
    <date>2015-08-05</date>
    <version>1.0.0</version>
    <description>Starterr is PressRoom Theme boilerplate.</description>
    <thumbnail>screenshot.png</thumbnail>
    <website>http://press-room.io/</website>
    <author>
        <name>thePrintLabs</name>
        <email>info@theprintlabs.com</email>
    </author>
    <layouts>
        <item>
            <name>basic article</name>
            <rule>content</rule>
            <description>default article layout</description>
            <path>layouts/basic-article.php</path>
        </item>
        <item>
            <name>cover</name>
            <rule>content</rule>
            <description>Cover layout</description>
            <path>layouts/cover.php</path>
        </item>
        <item>
            <name>toc</name>
            <rule>toc</rule>
            <description>Table of Contents theme file</description>
            <path>layouts/toc.php</path>
        </item>
    </layouts>
</theme>
```

> sample config.xml file from the Starterr theme

**Important Notes:**

- You must use regular permalinks to let **PressRoom** correctly handle url rewritings.
- Use the **Flush theme cache** option (PressRoom -> Settings) every time you move, delete or create new layout files.
