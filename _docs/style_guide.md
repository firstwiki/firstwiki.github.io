---
title: Style Guide
---

{% include stub %}

## Creating pages (wiki)

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

For more information, see https://jekyllrb.com/docs/permalinks/