---
layout: page
title: Evidex Development
tagline: 
---
{{% include JB/setup  %}}

Site Under Development

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

