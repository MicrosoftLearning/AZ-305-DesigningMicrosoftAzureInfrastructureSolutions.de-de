---
title: Online gehostete Anweisungen
permalink: index.html
layout: home
---

# Inhaltsverzeichnis

Links zu jeder Fallstudie sind unten aufgeführt.

## Fallstudien

{% assign casestudy = site.pages | where_exp:"page", "page.url contains '/Instructions/CaseStudy'" %}
| Modul | Fallstudie |
| --- | --- | 
{% for activity in casestudy  %}| {{ activity.casestudy.module }} | [{{ activity.casestudy.title }}{% if activity.casestudy.type %} - {{ activity.casestudy.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
