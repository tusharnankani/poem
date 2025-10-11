---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🌱

<p style="padding: 2em 1em; background: #f5f7ff; border-radius: 4px;">
  <!-- Take a look at <span style="font-weight: bold">[[Your first note]]</span> to get started on your exploration. -->
  Hey Shailja, Happy 24th Birthday ❤️
</p>


<strong></strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes %}
  <!-- {% for note in recent_notes limit: 5 %} -->
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
