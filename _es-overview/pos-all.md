---
layout: base
title:  'POS tags'
generated: 'true'
permalink: es/pos/all.html
---

# POS tags

{% include es-pos-table.html %}

----------

{% for p in site.es-pos %}
<h2><code>{{ p.title }}</code>: {{ p.shortdef }}</h2>
{% if p.content contains "<!--details-->" %}    
{{ p.content | split:"<!--details-->" | first }}
<a href="{{ p.title }}">See details</a>
{% else %}
{{ p.content }}
{% endif %}
<a href="{{ site.git_edit }}/_es-pos/{{ p.title }}.md" target="#">edit {{ p.title }}</a>
{% endfor %}