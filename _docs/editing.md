---
title: Editing FIRSTwiki (non-technical users)
layout: page
tags: contributing
---

<div class="alert alert-warning">
Because FIRSTwiki is not a traditional wiki, unfortunately it's currently
less user-friendly to edit than something like Wikipedia. As FIRSTwiki grows,
hopefully we'll be able to build easier ways for non-technical users to
contribute. Once you get the hang of it, it's not so bad.
</div>

## Create a github account

As all content is hosted on github, to edit it you must have a github account.
If you don't have an account, [go to Github to create an account](https://github.com/login)
and then login.

## Edit an existing page

Github provides an web-based editor to edit FIRSTwiki pages. First, open the
wiki page you wish to edit in your browser. In the top right of the window,
there will be an "Edit on GitHub" button. If you are logged in, this should
bring you directly to the online editor.

Once you're at the editor, you can make your changes to the document. You can
use these guides to learn more about how to structure the document content:

{% include by_tag collection=site.docs tag="content" %}

You may also find GitHub's documentation useful as well:

* [Writing on GitHub](https://help.github.com/categories/writing-on-github/)
* [Editing GitHub pages files](https://help.github.com/articles/editing-files-in-another-user-s-repository/)

### Saving your changes

Before you save (also called 'commit') your changes, click "Preview changes" on
editor to make sure your page is still formatted correctly. When you've made
sure that your page looks good, write a quick description of what you changed
underneath the "Commit changes" banner.

<div class="alert alert-warning">
<strong>Important:</strong> Make sure "Create a new branch for this commit and start a pull
request" is selected, otherwise your change will not be submitted to FIRSTwiki!
</div>

When everything looks good, click "Commit Changes" and your changes will be
saved to github.

Once your pull request has been created, a member of the [moderator
team](moderators) will have to approve the changes. Your changes will be
published immediately to the website once the pull request is merged.

## Creating new pages

This is possible to do from the github editor, but it's a bit more involved.
Until we write a guide for this, we encourage you to follow these steps
instead:

* (optional) Write out the content you're planning to contribute
* File a [new issue](https://github.com/firstwiki/wiki/issues/new) on the wiki
  GitHub site asking someone to create the page for you, optionally pasting
  in the content you created for the page.
