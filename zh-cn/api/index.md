---
layout: default
language: 'en'
version: '4.0'
title: 'API 索引'
---
## API 索引

{% for apiPage in site.pages %} {% assign stub = apiPage.name | slice: 0, 8 %} {% if "Phalcon_" == stub %} {% assign linkUrl = apiPage.name | replace: '', '' %} {% assign linkName = linkUrl | replace: '_', '\' %} * [{{ linkName }}](/{{ apiPage.version }}/{{ apiPage.language }}/api/{{ linkUrl }}) {% endif %} {% endfor %}