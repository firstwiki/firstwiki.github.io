---
title: Developing FIRSTwiki
layout: page
tags: contributing
---

<div class="alert alert-success">
    This page is targeted to those who want run FIRSTwiki locally; typically
    you're either a more technical user or you want to hack on FIRSTwiki at a
    more technical level: changing layouts, adding includes, changing the look
    and feel of the site, and other such tasks.
</div>

FIRSTwiki is a collection of git repositories. As such, working with it is a
little bit clunky at first, but we've created various scripts to make it easier
to work with the FIRSTwiki when doing local development.

### Environment setup

Currently all the documentation for setting up your development environment
is in the [README.md](https://github.com/firstwiki/_scripts/blob/master/README.md)
of the [_scripts repository](https://github.com/firstwiki/_scripts). Clone that
git repository and follow the instructions.

Unfortunately, the environment is only supported on OSX or Linux. However, we
welcome improvements to make it work on Windows. :)

### dev.sh

Once the environment is set up, there is a script called `dev.sh` which you can
use to do a lot of useful development tasks across all of the repositories.

To update all of your repos:

	./dev.sh pull

Or to build all sites:

	./dev.sh build

To serve an individual site locally, you can use jekyll to do this. Each repo has
'run_server.sh' script that makes the site available at `http://localhost:4000/URL`:

	cd wiki
	./run_server.sh

To serve all of the sites at the same time, then use this (requires all sites to
be built first!)

	./dev.sh serve_site

If you wish jekyll to watch the files and autoregenerate them when serving the
site, this will launch all of the sites and watch them:

	./dev.sh serve_site --watch

There's a lot more it can do... run it without any arguments, or read the script
to find more commands.

### jekyll-admin

The Gemfiles for the FIRSTwiki repos now include [jekyll-admin](https://github.com/jekyll/jekyll-admin),
which is intended to provide a web interface that allows you to edit your jekyll
site in a CMS-like environment. Unfortunately, because of some bugs it doesn't
quite support our layout... but hopefully this will be a good editing solution
in the future.

To access the admin site, go to `http://localhost:4000/admin/` (it's the same URL
for all FIRSTwiki repositories).


