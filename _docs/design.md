---
layout: page
title: FIRSTwiki Design
---

FIRSTwiki is not a traditional wiki, instead we have elected to build it around
github pages. As github pages isn't a perfect fit for a wiki, there are some
design considerations that were made as FIRSTwiki has been put together. This
page intends to explain some of this.

FIRSTwiki is not a single git repository, instead it is spread out across
multiple repositories:

* [firstwiki.github.io](https://github.com/firstwiki/firstwiki.github.io)
* [_common](https://github.com/firstwiki/_common)
* [wiki](https://github.com/firstwiki/wiki)
* [frc0000](https://github.com/firstwiki/frc0000)
* [frc1000](https://github.com/firstwiki/frc1000)
* [frc2000](https://github.com/firstwiki/frc2000)
* [frc3000](https://github.com/firstwiki/frc3000)
* [frc4000](https://github.com/firstwiki/frc4000)
* [frc5000](https://github.com/firstwiki/frc5000)
* [frc6000](https://github.com/firstwiki/frc6000)

The reason for this division is that jekyll can take a really long time to
parse and generate content, so they're split at natural division points so that
it doesn't take as long to build the content.

In the future as the amount of content gets larger, we may need to split it into
even more repositories.
