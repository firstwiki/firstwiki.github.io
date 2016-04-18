---
layout: default
title: Home
permalink: index.html
---

Welcome to [FIRSTwiki](/docs/about/), a _[FIRST](/wiki/first)_ encyclopedia that
anyone with a [github account](https://github.com/join) [can
edit](/docs/contributing)!

### Teams

* FRC:{% for num in site.data.teamdata.teamidx.frc %} [{{ num }}'s](/frc{{ num }}/) {% if forloop.last != true %}\|{% endif %}{% endfor %}

### Technical Topics

* Mechanical:
Motors \|
Pnuematics \|
Drive Train \|
Manufacturing
* Electrical: 
Control System \|
Programming


### Other Topics

* Team management \|
[FIRST Culture](/wiki/first-culture) \|
[Spirit](/wiki/spirit) \|
[Scouting](/wiki/scouting) \|
Organizations
* [People](/wiki/people)

### History

* FRC Games \| Control Systems \| Obsolete Parts

  
About FIRST
-----------

_[FIRST](/wiki/first)_ is an organization founded by inventor [Dean
Kamen](/wiki/dean-kamen) in 1989 as a way of getting students involved in and
excited about science and technology. _FIRST_ has grown from just a few hundred
students and mentors in 1992, and now reaches over 210,000 students worldwide.

FIRSTwiki news
--------------

[All news](/news/)

{% for post in site.posts limit: 3 %}
* {{ post.date | date_to_string }}: [{{ post.title }}]({{ post.url }})
{% endfor %}


