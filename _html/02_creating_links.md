### Creating Links

The [anchor](https://www.w3schools.com/tags/tag_a.asp) `<a>` tag defines a hyperlink, which is used to link from one page to another.

```html
<a href="site2.html" target="_blank" rel="next" title="Links to site two"> Site Two </a>
```
###### Linking to different directories

| href=""| Description |
| ------------------|-----------|
| `../`             | Link to one up directory |  
| `/..`             | Link to one down directory |  
| `https://..`      | Link to external pages using an absolute link |
| `../1255xy78.pdf` | Link to downloadable resources._Use the attribute `download="content.pdf"` to change the name of the `1255xy78.pdf` file to `content.pdf`._|
| `#..`             | Link to section of page using the pound `#` character. The `..` needs to be defined by `id=`. For example, to go to section 2 of the page (i.e `<h2> Section Two id="two" <h2>`) use `#two`.

 The **target** attribute is typically used to open a page in a new window or tab, or to control where a page opens within a frame set.

| Value	| Description |
| ------ |-----------|
| ` _blank`  | Load in a new window |
| `_self`	   | Load in the same frame as it was clicked |
| `_parent`  | Load in parent frameset |
| `_top`	   | Load in the full body of the window |
| `framename`| Load in a named frame |

The **rel** attribute specifies the relationship between the current document and the linked document

| Value	| Description |
| ------ |-----------|
| `download`   | Indicates that this link will download an external file. **Newly added in HTML5**, _ So support for it may be limited at the time this document was written_ |
| `alternate`  | Provides a link to an alternate representation of the document (i.e. print page, translated or mirror) |
| `author`	   | Provides a link to the author of the document |
| `bookmark`   | Permanent URL used for bookmarking |
| `external`	 | Indicates that the referenced document is not part of the same site as the current document |
| `help`       | Provides a link to a help document |
| `license`    | Provides a link to copyright information for the document |
| `next`       | Provides a link to the next document |
| `nofollow`   | Links to an unendorsed document, like a paid link. ("nofollow" is used by Google, to specify that the Google search spider should not follow that link) |
| `noreferrer` | Requires that the browser should not send an HTTP referer header if the user follows the hyperlink |
| `noopener`   | noopener	Requires that any browsing context created by following the hyperlink must not have an opener browsing context |
| `prev`       | The previous document in a selection |
| `search`     | Links to a search tool for the document |
| `tag`        | A tag (keyword) for the current document |

The **title** attribute provides additional information about a link element.This helps make links more accessible by giving the link a title, which can be read and interpreted by assistive devices, search engines or other content readers. It's almost always a good idea to use a title attribute when creating a link to another page or resource.
