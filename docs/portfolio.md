---
layout: page
title: Portfolio
permalink:
---

I'm not completely done filling in all my projects, I'll remove this message once it's up to date.

{% for project in site.portfolio reversed%}

<hgroup id={{ project.slug }}>
    <h3>{{ project.name }}</h3>
    <p>
        {{ project.client }}
        {%- if project.team -%}&nbsp;/&nbsp;{{ project.team}}{%- endif -%}
        {%- if project.budget -%}&nbsp;/&nbsp;{{ project.budget}}{%- endif -%}
    </p>
</hgroup>

{%- if project.content -%}
{{ project.content }}
{%- endif -%}

<hr/>

{% endfor %}