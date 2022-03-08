---
title: News
---
# News

{% assign en_news_posts = site.categories.news | where: 'language', 'en' %}
{% for post in en_news_posts %}
## {{ post.title }} <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date: "%b %d, %Y" }}</time>

{{ post | inspect }}

{{ post.content }}
{% endfor %}
