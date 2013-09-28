# Markdown Essay

An alternative to the [Essay](https://tent.io/docs/post-types#essay) post type, using Markdown instead of HTML.


#### Schema

| Property | Required | Type | Description |
| -------- | -------- | ---- | ----------- |
| `title` | Optional | String | The title of the post. |
| `excerpt` | Optional | String | An excerpt of the post in Markdown format to be displayed when the whole post is not available. |
| `body` | Required | String | The body of the post in Markdown format. Renderers may sanitize the output. |

#### Issues

- Standard Markdown, Tent Flavored Essay Markdown, or (for the sake of argument) support for any flavor of Markdown?
- Being compatible with Tent Flavored Markdown for `status` posts would allow apps to automagically "upgrade" a `status` post to this post type if it becomes larger than 256 characters. Though, `status` post's Tent Flavored Markdown is incompatible with standard Markdown (syntax for emphasis and strikethrough)..
- Might not get support from all Tent blogging apps (there's already the Essay post type for HTML only). Far from ideal if users are limited to "Essay Markdown compatible" apps to use this. Two-way conversion between HTML<->Markdown could offer compatibility between the two post types, but sounds like a dirty workaround.
- Markdown is a living markup language with several dialects as well as varying output depending on the implementation used. Something to be aware of.

#### Links

- [Tent issue suggesting adding Markdown to Essay](https://github.com/tent/tent.io/issues/200) - Background to this post type
- [Markdown Community](http://markdown.github.io/) - Unofficial page for the Markdown community
- [Official project page](http://daringfireball.net/projects/markdown) - Original spec, last updated in 2004
- [W3C Community Group](http://www.w3.org/community/markdown/) - Has been dormant since late 2012
- [Babelmark 2](http://johnmacfarlane.net/babelmark2/) - Tool to compare Markdown implementations
