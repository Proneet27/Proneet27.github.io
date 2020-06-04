---
layout: archive
permalink: /data-science/
title: "Data Science Posts"
author_profile: true
header:
  image: "/images/ds.jpg"
---
{% include base_path %} {% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %} {% assign posts = group_items[forloop.index0] %}

{{ tag }}
{% for post in posts %} {% include archive-single.html %} {% endfor %} {% endfor %}
