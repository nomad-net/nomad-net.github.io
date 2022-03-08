---
title: News
---
# News

{% assign news_posts = site.posts | where: 'category', 'news' %}
{% for post in site.posts %}
## {{ post.title }}

{{ post.content }}
{% endfor %}
