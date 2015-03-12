# Hooks

During a package creation or while performing a preview action, **PressRoom** parse all the content items connected to an Edition

**Note:**
This process applies just to content items included in the **flatplan** and in ``visible`` status

---

####pr\_packager\_run\__{post\_type}_
Before writing the html output of each post type.

``` php
/**
* @param object $post
* @param string $edition_dir ( directory contenente i file del pacchetto )
* @void
*/
function package_my_custom_post_type( $post, $edition_dir ) {

	// Do stuff
}

add_action( 'pr_packager_run_{custom_post_type}', package_my_custom_post_type , 10, 2 );
```
---

####pr\_packager\_generate\_book
Hook to the ``book.json`` file creation. Could be used to delete, modifiy or add new keys.

``` php

/**
* @param array $press_options l'array di tutte le opzioni del book.json
* @param object $post
* @param string $edition_dir ( directory contenente i file del pacchetto )
* @void
*/
function add_my_custom_post_type_to_book_json( &$press_options, $post, $edition_dir ) {
	// Do stuff
}

add_action( 'pr_packager_generate_book', add_my_custom_post_type_to_book_json , 10, 2 );
```
---

####pr\_preview\__{post\_type}_
Hook to the previewer. Could be used to modify a post type output before its visualization.

``` php

/**
* @param string $page_url
* @param object $edition
* @param object $post
* @void
*/
function add_my_custom_post_type_to_previewer( &$page_url, $edition, $post ) {
	// Do stuff
}

add_action( 'pr_preview_{custom_post_type}', add_my_custom_post_type_to_previewer , 10, 3 );
```
---

####press\_flush\_rule
Hook to the PressRoom activation. If you're extending **PressRoom** declaring new post types under its structure you'll need to use this hook to correctly handle url rewritings.

``` php
function custom_post_type() {

	$args = array(
    	'your-option' => '...'
    );
	register_post_type( 'post_type', $args );
}
// standard registration wordpress hook
add_action( 'init', 'custom_post_type', 0 );

// pressroom flush rules hook
add_action( press_flush_rules, 'custom_post_type', 0 );

```
Customizing the default theme
