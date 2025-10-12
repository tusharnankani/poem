---
layout: page
title: Home
id: home
permalink: /
---

<!-- # Welcome! 🌱 -->

This is an archive of stillness, movement, and the words in between.

<p style="padding: 1.5em 1em; background: #f5f7ff; border-radius: 4px;">
  <!-- Take a look at <span style="font-weight: bold">[[Your first note]]</span> to get started on your exploration. -->
  Hey Shailja, Happy 24th Birthday ❤️
</p>


<strong>My Writings</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "date" | reverse %}
  {% for note in recent_notes %}
    <li>
      {{ note.date | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
