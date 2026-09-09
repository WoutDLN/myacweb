---
layout: page
title: Talks
permalink: /talks/
---

{% assign talks = site.talks | sort: "date" | reverse %}

{% assign current_year = "" %}

{% for talk in talks %}

  {% assign talk_year = talk.date | date: "%Y" %}

  {% if talk_year != current_year %}

    {% unless forloop.first %}
  </ul>
    {% endunless %}

  <h2>{{ talk_year }}</h2>
  <ul>

    {% assign current_year = talk_year %}

  {% endif %}

  <li>
    <a href="{{ talk.url |_url }}" target="_blank">
      {{ talk.title }}
    </a> ({{ talk.type }})
  </li>

{% endfor %}

</ul>