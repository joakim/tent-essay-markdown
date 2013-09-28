# Markdown Essay

An alternative to the [Essay](https://tent.io/docs/post-types#essay) post type, using Markdown instead of HTML.


#### Schema

| Property | Required | Type | Description |
| -------- | -------- | ---- | ----------- |
| `title` | Optional | String | The title of the post. |
| `excerpt` | Optional | String | An excerpt of the post in Markdown format to be displayed when the whole post is not available. |
| `body` | Required | String | The body of the post in Markdown format. Renderers may sanitize the output. |

#### Issues

- Should it support only standard Markdown, Tent Flavored Markdown also, or (for the sake of argument) any flavor of Markdown? Keep in mind the requirements for apps wanting to support this post type.
- Being compatible with Tent Flavored Markdown (used by `status` posts) would allow apps to automagically "upgrade" a `status` post to this post type if it becomes larger than 256 characters. (However, see next point..)
- [Tent Flavored Markdown](https://tent.io/docs/post-types#markdown) is incompatible with standard Markdown (syntax for emphasis and strikethrough differ, linebreak handling is compatible with most modern flavors however).
- This post type wouldn't get support from all Tent blogging apps, as there's already the `essay` post type that supports HTML only. Users would be limited to "Markdown Essay" compatible apps when using this post type.
- Other users may also only be able to subscribe to HTML based `essay` posts. Apps creating Markdown Essay posts may therefore want to store a compiled HTML copy as an `essay` post to cater to those. Users would obviously not want to edit this copy!
- Two-way conversion between HTML<->Markdown could offer compatibility with the `essay` type, and allow editing of either "version". But this sounds like a very hairy workaround.
- Markdown is a non-standardized and living markup language with several dialects as well as differing output depending on the implementation used. Just something to be aware of.

#### Links

- [Tent issue for adding Markdown support to Essay](https://github.com/tent/tent.io/issues/200) - Background to this post type
- [Markdown Community](http://markdown.github.io/) - Unofficial page for the Markdown community
- [Official project page](http://daringfireball.net/projects/markdown) - Original spec, last updated in 2004
- [W3C Community Group](http://www.w3.org/community/markdown/) - Has been dormant since late 2012
- [Babelmark 2](http://johnmacfarlane.net/babelmark2/) - Tool to compare Markdown implementations
