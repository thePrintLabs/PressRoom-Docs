# PressRoom API

## Variables
The following variables are initialized right before the posts parsing thus they're globally available in PR theme files: 

- `$edition` **\_object\_**     
`object(WP_Post)` Contains data from the current **Edition**

- `$editorial_project_id` **\_string\_**   
URI of the **Edition** active theme.

- `$pr_package_type` **\_string\_**  
Return the current packager type ('hpub', 'web', etc.)

- `$pr_theme_url`**\_string\_**  
Absolute URL of the *Edition* active theme.

## Functions

---
```php
pr_get_edition_posts( $edition, $only_enabled )
```
Returns the array of content items connected to an Edition.

- ```$edition - _object_```
	The whole *Edition* object
- **$only\_enabled** - _boolean_
	Include/Esclude posts marked as "hidden" in the flatplan

---

```php
pr_prev( $post_id, $edition_id )
```

Returns the previous post url following the flatplan order.

- **$post\_id** - _int_
Current post ID
- **$edition\_id** - _int_
Current Edition ID

---

```php
pr_next( $post_id, $edition_id )
```

Returns the next post url following the flatplan order.

- **$post\_id** - _int_
Current post ID
- **$edition\_id** - _int_
Current Edition ID

---

```php
pr_get_sharing_link( $post_id )
```

Returns the sharing url for the current post.

- **$post_id** - _int_
Current post ID

[1]:	https://github.com/bakerframework/baker/wiki/Book-protocol "book protocol"