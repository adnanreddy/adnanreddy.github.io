---
layout: page
title: Writing
permalink:
---

<p>Subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p>

{%- for post in site.posts-%}
    {%- assign date_format = "%B %-d, %Y" -%}
    <p><strong><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></strong> <i>{{ post.date | date: date_format }}</i></p>
{%- endfor -%}

{%- if site.posts.size == 0 -%}
<i>Coming soon...</i>
{%- endif -%}