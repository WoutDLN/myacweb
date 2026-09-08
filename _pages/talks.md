---
layout: page
title: Talks
permalink: /talks/
---

{% assign talks = site.talks | sort: "date" | reverse %}

<ul>

{% for talk in talks %}
<li>
  <a href="{{ talk.url| relative_url }}">{{ talk.title }}</a>

  ({{ talk.date | date: "%Y" }})

</li>

{% endfor %}

</ul>