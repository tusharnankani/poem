---
layout: page
title: Home
id: home
permalink: /
---

This is an archive of stillness, movement, and the words in between.

<h2>My Writings</h2>

{% assign notes_by_year = site.notes | group_by_exp: "note", "note.date | date: '%Y'" | sort: "name" | reverse %}
{% for year in notes_by_year %}
<h3>{{ year.name }}</h3>
<ul>
  {% assign items = year.items | sort: "date" | reverse %}
  {% for note in items %}
    <li>
      {{ note.date | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>
{% endfor %}

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
