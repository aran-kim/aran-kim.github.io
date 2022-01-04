---
title: "컴퓨터 사이언스"
layout: categories
permalink: /categories/cs/
author_profile: true
sidebar:
  nav: "categories"
---
computer science study

{% assign posts = site.categories.cs %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}