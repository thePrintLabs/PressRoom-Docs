# Theming

In **PressRoom** you are able to set custom themes for each *Editorial Project*. This setting could be overwritten per each *Edition* in the **Edition Meta** tab.

Developing **PressRoom** themes is quick and easy since they inherits almost the same logic used for [Wordpress Theme Development ](http://codex.wordpress.org/Theme_Development/ "Wordpress Theme Devepopment")

###File Structure

**PressRoom** themes resides inside the ```/pressroom/themes/``` folder.

Themes are essentially made of **layout files** and assets (css, js, fonts, images, etc. ). Everything has been built for maximum flexibility, thus you are not forced to follow a specific folder structure to organize this contents.


### functions.php
Each **PressRoom** theme could use his own `functions.php` file. Place it wherever make sense for you, it will be recognized automatically.

###Layout files

A layout files require a front matter in order to be recognized by **PressRoom**

``` yaml
/*
* theme:        mytheme
* rule:         content
* name:         sample-layout
* description:  A sample layout file
*/
```
**theme:** You awesome theme name namespace.
**rule:** There are three kind of rules: ```content```,```toc``` and ```cover```
**name:** Unique layout file name (to be shown in the Edition **Flatplan**)
**description:** self explanatory.

Everything here should be lowercase except for **descrition**.

####Rule Attribute

As said the rule attribute could be:

- ```content``` A layout file used to render content items (post, pages, custom post types)
- ```toc``` A layout files used to render the **Table of Contents** inside a Baker powered application.
-  ```cover``` A special rule to help you keep track of a cover layout for your Edition.

You could define as many layout as you wish with the rule ```content```. Then, you'll be able to select which layout to use per each item in your **flatplan**

###Table of Content ( TOC )

>Baker TOC options can be customized inside *Editorial Project* -> TOC

``` php
/*
* theme: Pressroom
* rule: toc
*/
```

 **Example:**


```
 <?php if ( $posts->have_posts() ) : ?>
		<?php while ( $posts->have_posts() ) : $posts->the_post(); ?>
			<a href="<?php echo get_permalink(); ?>">
				<?php the_title(); ?>
			</a>
	<?php endwhile; ?>
<?php endif; ?>
```
**Important Notes:**

- You must use regular permalinks to let **PressRoom** correctly handle url rewritings.
- Use the **Flush theme cache** option (PressRoom -> Settings) every time you move, delete or create new layout files.
