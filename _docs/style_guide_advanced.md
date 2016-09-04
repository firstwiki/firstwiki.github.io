---
layout: page
title: Style Guide (advanced)
tags: content
---

This covers various things you can add to your Markdown content to make content
more uniform and save you some typing.

Categories
----------

It is often useful to have a set of pages that are associated together in a
category, so that we can create automatically updated lists of those pages.

You can specify that a page belongs to one or more categories by adding a
`tags` variable to the '[front matter](https://jekyllrb.com/docs/frontmatter/)'
that is found at the beginning of most pages:

```text
---
title: Page Title
tags: category1 category2
---
```

You can display a listing of all pages that match that category using this
include on a page somewhere:

```liquid {% raw %}
{% include by_tag collection=site.tech tag="category1" %}
{% endraw %}```

The 'collection' parameter references the collection that the page is in
(this is usually the topmost parent directory of the page). In this case the
page is in the 'tech' collection

The 'tag' parameter names the specific tag that you want to create a list of

Redirect Pages
--------------

Sometimes pages get renamed, or there are multiple names for the same topic. In
these cases, a redirect page can be created. The entire content of the page
should look like this:

```
---
layout: redirect
redirect_to: new_page_name
---
```


Includes
--------

We use jekyll's include mechanism to provide standard commonly used templates
that can be included on FIRSTwiki pages. Here is a list of the includes, and a
description of when/where to use them.

### Cleanup

```liquid
{% raw %}{% include cleanup %}{% endraw %}
```

#### Output

{% include cleanup %}

#### Description

Displays a notice that this article is a bit messy and needs some love. 

<hr>

### Historical

```liquid
{% raw %}{% include historical %}{% endraw %}
```

#### Output

{% include historical %}

#### Description

Displays a notice that this section of an article contains information that
is retained for historical reasons, and does not need to be updated. This is
**not** the same as outdated information that needs to be updated. That
should use the outdated-warning include instead.

<hr>

### Outdated warning

```liquid
{% raw %}{% include outdated-warning %}{% endraw %}
```

#### Output

{% include outdated-warning %}

#### Description

Displays a notice that this section of an article contains information that
while may be useful, is most likely outdated.

<hr>

### POV
```liquid
{% raw %}{% include POV %}{% endraw %}
```

#### Output

{% include POV %}

#### Description

Displays a notice that this article is a disputed and should be updated.

<hr>

### Stub

```liquid
{% raw %}{% include stub %}{% endraw %}
```

#### Output

{% include stub %}

#### Description

Displays a notice that this article is a stub and should be updated.

<hr>

### Todo

```liquid
{% raw %}{% include TODO %}{% endraw %}
```

#### Output

{% include TODO %}

#### Description

Display a notice that a specific section of a page needs some more work. This is
different from a note that the *entire* page needs work; prefer the stub or
cleanup includes in those cases.

### Wikipedia links

```liquid
{% raw %}{% include wikilink topic="Topic" %}{% endraw %}
```

#### Output

{% include wikilink topic="Topic" %}

#### Description

FIRSTwiki is not meant to replace something like Wikipedia, but rather it is
meant to supplement it with FIRST-specific information. When you want to provide
a pointer to a wikipedia page as the primary source of information, use this
include. For normal references, use the same mechanism as any other external
links.


## Other

Because FIRSTwiki is a jekyll-based site, you can take advantage of any of the
capabilities that jekyll offers. There are several places where FIRSTwiki takes
advantage of these capabilities that are not documented here.

For more information aout jekyll, refer to their documentation at
[http://jekyllrb.com/docs/](http://jekyllrb.com/docs/).
