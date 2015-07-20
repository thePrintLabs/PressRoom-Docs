# PressRoom API

#### Variables

- **$edition - _object_**
WP\_Post object (pr\_edition) containing all current *Edition* data.

- **$pr\_theme\_url - _string_**
Absolute URL of the *Edition* actives theme.

#### Functions

---

\`\`\` php
pr\_get\_edition\_posts( $edition, $only\_enabled )
\`\`\`
Returns the array of content items connected to an Edition.

- **$edition** - _object_
	The whole *Edition* object
- **$only\_enabled** - _boolean_
	Include/Esclude posts marked as "hidden" in the flatplan

---

\`\`\` php
pr\_book( $edition\_id )
\`\`\`

Returns a Baker Editon Url [book://][1]

- **$edition\_id** - _int_
Edition ID

---

\`\`\` php
pr\_prev( $post\_id, $edition\_id )
\`\`\`

Returns the previous post url following the flatplan order.

- **$post\_id** - _int_
Current post ID
- **$edition\_id** - _int_
Current Edition ID

---

\`\`\` php
pr\_next( $post\_id, $edition\_id )
\`\`\`

Returns the next post url following the flatplan order.

- **$post\_id** - _int_
Current post ID
- **$edition\_id** - _int_
Current Edition ID

---

\`\`\` php
pr\_get\_sharing\_link( $post\_id )
\`\`\`

Returns the sharing url for the current post.

- **$post\_id** - _int_
Current post ID

[1]:	https://github.com/bakerframework/baker/wiki/Book-protocol "book protocol"