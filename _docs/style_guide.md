---
layout: page
title: Style Guide
tags: content
---

## Formatting pages (wiki)

As FIRSTwiki is not a traditional wiki, the format differs slightly from what
Wikipedia uses. Here's some simple examples to get you going:

```
## Use this header first

This is some content in a paragraph.
This is the same paragraph.

This is a separate paragraph. And a link to a [website](https://firstwiki.github.io/).

### A smaller header

*This sentence is italicized*.

**This sentence is bold**.

* List item 1
* List item 2

Here's a table:

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

```

And these render like so:

<hr>

## Use this header first

This is some content in a paragraph.
This is the same paragraph.

This is a separate paragraph. And a link to a [website](https://firstwiki.github.io/).

### A smaller header

*This sentence is italicized*.

**This sentence is bold**.

* List item 1
* List item 2

Here's a table:

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

<hr>

### More formatting

If you need other types of formatting, there's a lot of documentation out
there. You can also [check out the original Markdown specification](https://daringfireball.net/projects/markdown/basics).

### Linking to other pages (wiki)

To link to a particular page in the wiki section you can do 

```markdown
[text](/wiki/slug)
```

Or if you're linking from a wiki article:

```markdown
[text](slug)
```


### On titles and slugs

In the [/wiki](/wiki) section, there are a lot of pages. If we put them all in a
flat directory structure, it would get really annoying to edit them, and once
there are enough pages then github will refuse to display them. To solve this, we
put the pages in a hierarchical directory structure so they're easier to
navigate and find. 

However, it's also annoying to create links to `/wiki/nontech/culture/spirit/`.
As a compromise, all URLs of pages in the wiki section are `/wiki/:slug`, so to 
link to a particular page in the wiki section you can do `[text](/wiki/slug)` or
if you're linking from a wiki article, `[text](slug)`.

A slug is defined as the lowercase filename of the document where any character
except numbers and letters are replaced with hyphens.

<div class="alert alert-danger">
To prevent breaking external links to content, do <strong>NOT</strong> rename
articles without adding a custom slug matching the old path!
</div>

For more information, see [https://jekyllrb.com/docs/permalinks/](https://jekyllrb.com/docs/permalinks/)

### Tips

* Prefer to use [liquid templates](https://jekyllrb.com/docs/templates/) and
  [front-matter](https://jekyllrb.com/docs/frontmatter/) to display repetitive
  content, instead of copy/pasting the same stuff across multiple pages

* Check out the [advanced style guide](style-guide-advanced) for more stuff!