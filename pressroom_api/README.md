# PressRoom API

#### Variables

- **$edition - _object_**
WP_Post object (pr_edition) containing all current *Edition* data.

- **$pr\_theme\_url - _string_**
Absolute URL of the *Edition* active theme.

#### Functions

---

``` php
pr_get_edition_posts( $edition, $only_enabled )
```
Returns the array of content items connected to an Edition.

- **$edition** - _object_
    The whole *Edition* object
- **$only\_enabled** - _boolean_
    Include/Esclude i post marcati come nascosti sul flatplan

---

``` php
pr_book( $edition_id )
```

Returns a Baker Editon Url [book://](https://github.com/bakerframework/baker/wiki/Book-protocol "book protocol")

- **$edition\_id** - _int_
Edition ID

---

``` php
pr_prev( $post_id, $edition_id )
```

Returns the previous post url following the flatplan order.

- **$post\_id** - _int_
Current post ID
- **$edition\_id** - _int_
Current Edition ID

---

``` php
pr_next( $post_id, $edition_id )
```

Returns the next post url following the flatplan order.

- **$post\_id** - _int_
Current post ID
- **$edition\_id** - _int_
Current Edition ID

---

``` php
pr_get_sharing_link( $post_id )
```

Returns the sharing url for the current post.

- **$post\_id** - _int_
Current post ID

