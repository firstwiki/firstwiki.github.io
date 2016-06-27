---
layout: page
title: Contributing to FIRSTwiki
---

FIRSTwiki is an open project that all members of the FIRST community can easily
and quickly contribute to. We believe that by providing open content we can
better serve the FIRST community.

How to contribute
-----------------

FIRSTwiki is not a traditional wiki, instead it's a bunch of
[Markdown](https://daringfireball.net/projects/markdown/) formatted files stored
in a git repository that are rendered and served via [github
pages](https://help.github.com/categories/writing-on-github/) (via
[jekyll](https://jekyllrb.com/)). There are two main different ways to contribute:

* Using the Github editor
* Using a local text editor

Using the Github editor is the much simpler option if you are just starting out
editing, or you are editing just a singular page. If you are editing a large
batch of files, or need to add a new page, you should clone the repository locally and use a text editor,
such as [atom](https://atom.io), to make your changes.

To start off both processes, you have to [create a Github account](https://github.com/login), and [make a fork](https://help.github.com/articles/fork-a-repo/)
of the relative FIRSTwiki repository. There are [six repositories for team numbers and their pages](https://github.com/firstwiki), [one for main wiki content](https://github.com/firstwiki/wiki), and [one for the central documentation
and other vital data for the wiki](https://github.com/firstwiki/firstwiki.github.io).
GitHub will automatically create a fork for you if you are using the online editor.

To use the Github in browser editor, open the wiki page you wish to edit in your browser.
In the top right of the window, there will be an "Edit on GitHub" button. This
should bring you directly to the online editor. Make your changes to the article,
using [Markdown](https://daringfireball.net/projects/markdown/). Before you commit
your changes, click "Preview changes" on the tab bar on this web page to make sure your
page is still formatted correctly. When you've made sure that your page looks fine,
write a quick description of what you changed underneath the "Commit changes" banner.
Make sure "Create a new branch for this commit and start a pull request" is selected,
and your changes will be automatically made and a pull request has been submitted
so a [moderator](/docs/moderators) can approve your changes.

To use your own editor, clone your fork that you created of the repository online
to your computer. [Here](https://guides.github.com/activities/forking/) is a guide on how
to do that in the [Github Desktop](https://desktop.github.com) client, or
[here](https://help.github.com/articles/fetching-a-remote/) is a guide on how to do it
on the command line. Make your changes, commit them, push them back to GitHub, then
create a pull request through the GitHub web interface. 

Once your pull request has been created, a member of the [moderator
team](/docs/moderators) will have to approve the changes. Your changes will be
published as soon as the pull request is merged.

See also:

* [FIRSTwiki Style Guide](/docs/style-guide)
* [Github's documentation for editing github pages files](https://help.github.com/articles/editing-files-in-another-user-s-repository/)

What to contribute
------------------

See our [content guidelines](/docs/content/) for more information.

Tips
----

* Prefer to use [liquid templates](https://jekyllrb.com/docs/templates/) and
  [front-matter](https://jekyllrb.com/docs/frontmatter/) to display repetitive
  content, instead of copy/pasting the same stuff across multiple pages
