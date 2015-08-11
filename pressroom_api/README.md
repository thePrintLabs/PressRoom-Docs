# PressRoom API

## Variables
The following variables are initialized right before the posts parsing thus they're globally available in PR theme files: 

- `$edition` **object**     
`object(WP_Post)` Contains data from the current **Edition**

- `$editorial_project_id` **string**   
URI of the **Edition** active theme.

- `$pr_package_type` **string**  
Return the current packager type ( 'hpub', 'web', ... )

- `$pr_theme_url` **string**  
Absolute URL of the *Edition* active theme.

### Toc additional variable

Inside the theme file identified by the rule `toc` we automatically expose the `$edition_posts` variable which is used to loop through the issue's content items to build the main navigation. The same result could be achieved using the `pr_get_edition_posts` function documented below. 

## Functions

```php
pr_get_edition_posts( $edition, $only_enabled )
```
Returns the array of content items connected to an Edition.

- ```$edition - _object_```
	The whole *Edition* object
- **$only_enabled** - _boolean_
	Include/Esclude posts marked as "hidden" in the flatplan


```php
pr_prev( $post_id, $edition )
```

Returns the previous post url following the flatplan order.

- **$post_id** - _int_
Current post ID
- **$edition_id** - _int_
Current Edition ID


```php
pr_next( $post_id, $edition )
```

Returns the next post url following the flatplan order.

- **$post_id** - _int_
Current post ID
- **$edition_id** - _int_
Current Edition ID


```php
pr_get_sharing_url( $post_id )
```

Returns the sharing url for the current post.

- **$post_id** - _int_
Current post ID

[1]:	https://github.com/bakerframework/baker/wiki/Book-protocol "book protocol"

