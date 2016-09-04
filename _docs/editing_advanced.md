---
title: Editing FIRSTwiki (technical users)
layout: page
tags: contributing
---

<div class="alert alert-info">
Using the Github web-based editor is a much simpler option if you are just
starting out editing, or you are only editing a single page. See the <a
href="editing">non-technical user's guide</a> for details.
</div>

## Setup tasks

### Create a github account

As all content is hosted on github, to edit it you must have a github account.
If you don't have an account, [go to Github to create an account](https://github.com/login)
and then login.

### Fork the repo(s)

There are [six repositories for team numbers and their
pages](https://github.com/firstwiki), [one for main wiki
content](https://github.com/firstwiki/wiki), and [one for the central
documentation and other vital data for the
wiki](https://github.com/firstwiki/firstwiki.github.io). Determine which
repository you wish to edit, and [make a
fork](https://help.github.com/articles/fork-a-repo/).

Clone your fork that you created of the repository to your computer.
[Here](https://guides.github.com/activities/forking/) is a guide on how to do
that in the [Github Desktop](https://desktop.github.com) client, or
[here](https://help.github.com/articles/fetching-a-remote/) is a guide on how to
do it on the command line.

## Editing the content

Next, you'll want to fire up your [favorite editor](https://atom.io) to modify
the file you wish to change, or create a new file. You can use these guides to
learn more about how to structure the document content:

{% include by_tag collection=site.docs tag="content" %}

Make your changes, commit them via git, push them back to GitHub, then
[create a pull request](https://help.github.com/articles/creating-a-pull-request/).

Once your pull request has been created, a member of the [moderator
team](moderators) will have to approve the changes. Your changes will be
published immediately to the website once the pull request is merged.

### Viewing your changes locally

<div class="alert alert-warning">These instructions only tested on OSX and Linux</div>

When editing locally, you will probably want to check your changes in your web
browser. If you have ruby installed, this is pretty simple. Run the following
commands in the repo directory:

```sh
gem install bundler
bundle install
```

Once that is done, you can start your site locally using the following command:

```sh
./run_server.sh`.
```

Once the server is running, you can point your web browser at `http://localhost:4000/URL`.

Each time you save a page while the server is running, it will recompile the site. To view the
changes, refresh the page to see the new changes. 

## Advanced development

If you want to make more complex changes, [check out our page for developers](developing).
