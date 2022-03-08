---
title: News
---
# News

{% assign en_news_posts = site.categories.news | where: 'language', 'en' %}
{% for post in en_news_posts %}
## {{ post.title }}

{{ post | inspect }}

{{ post.content }}
{% endfor %}
