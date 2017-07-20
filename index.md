---
layout: default
title: Home
permalink: index.html
---

Welcome to [FIRSTwiki](/docs/about/), a _[FIRST](/wiki/first)_ encyclopedia that
anyone with a [github account](https://github.com/join) [can
edit](/docs/contributing)!

<div class="alert alert-info">
You may notice there's not a lot of content here! There's a ton of content that needs to be copied
from the <a href="https://github.com/firstwiki/original_archive" class="alert-link">original FIRSTwiki</a>
and it would be wonderful if you could copy a few useful articles to this site! See our
<a class="alert-link" href="/docs/contributing">contributing notes</a> for more details!
</div>

### Teams

* FRC:{% for num in site.data.teamdata.teamidx.frc %} [{{ num }}'s](/frc{{ num }}/) {% if forloop.last != true %}\|{% endif %}{% endfor %}

### Technical Topics

* **Mechanical**:
  * [Motors](/wiki/motors)
  * [Pneumatics](/wiki/pneumatics)
  * Manufacturing
* [**Electrical**](/wiki/electrical):
  * [Control System](/wiki/control-system)
* [**Programming**](/wiki/programming):
  * [Robot Code Directory](/wiki/robot-code-directory)
  * [Software](/wiki/software)
* [**Design**](/wiki/design):
  * [Drive Train](/wiki/drive-train)
  * [Intakes](/wiki/intake)
  * [Manipulators](/wiki/manipulator)
  * [Shooters](/wiki/shooter)
* [**All technical topics**](/wiki/tech)


### Other Topics

* [FIRST Culture](/wiki/first-culture)
* [Fundraising](/wiki/fundraising)
* [Spirit](/wiki/spirit)
* [Scouting](/wiki/scouting)
* Organizations
* [People](/wiki/people)
* [**All non-technical topics**](/wiki/nontech)

#### History

* [FRC Games](/wiki/frc-games)
* Control Systems
* [Obsolete Parts](/wiki/obsolete-parts)
* [Kit of Parts](/wiki/kit-of-parts)
* [FRC Rules](/frcrules)

  
About FIRST
-----------

_[FIRST](/wiki/first)_ is an organization founded by inventor [Dean
Kamen](/wiki/dean-kamen) in 1989 as a way of getting students involved in and
excited about science and technology. _FIRST_ has grown from just a few hundred
students and mentors in 1992, and now reaches over 400,000 students worldwide.

FIRSTwiki news
--------------

[All news](/news/)

<ul>
{% for post in site.posts limit: 5 %}
<li>{{ post.date | date_to_string }}: <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}


<script>
// this bit of script loads JSON for each project, and displays page counts
$(document).ready(function(){
  // wiki data
  $.getJSON("/wiki/site-data.json", function(data){
    $('#other-topics').append(" (" + (data.nontech + data.people) + " pages)");
    $('#technical-topics').append(" (" + data.tech + " pages)");
    $('#history').append(" (" + data.history + " pages)");
  });
  
  // count the team pages
  var teamdata = [{% for td in site.data.teamdata.teamidx.frc %}'{{ td }}'{% if forloop.last == false %},{% endif %}{% endfor %}];
  
  for (var i = 0; i < teamdata.length; i++) {
      teamdata[i] = $.getJSON('/frc' + teamdata[i] + '/site-data.json', function(d) {return d});
  }
  
  $.when.apply($, teamdata).done(function() {
    var teamPages = 0;
    for (var i = 0; i < arguments.length; i++) {
        teamPages += arguments[i][0].frc;
    }
    $('#teams').append(" (" + teamPages + " pages)")
  });
});
</script>
