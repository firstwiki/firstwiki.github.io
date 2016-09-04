---
layout: page
title: Style Guide (team pages)
tags: content
---

Team pages are just like any other page, except that they tend to have a lot of
data in the [YAML front matter](https://jekyllrb.com/docs/frontmatter/) section
of the page. By providing the data in a structured format, it allows automated
tools to easily process and format the data.

Here's an example team showing many of the available data elements:

```text
---
title: FRC Team 0
team:
  type: FRC
  number: 0
  name: Name of the team
  rookie_year: 1993
  location: Somewhere, Anywhere
  sponsors:
  - Sponsor 1
  - Sponsor 2
  links:
    Website: 
    Github: https://github.com/FRC0000
robot_code:
  2016:
  - Robot:
    - https://github.com/FRC0000/2016
    - C++
  - Vision:
    - https://github.com/FRC0000/2016-vision
    - C++
---

Normal FIRSTwiki markdown syntax shows up here.
    
```

{% include TODO %}
    
## After the front matter

The text here is just like any other wiki page, see the [normal style guide](style-guide)
for details.