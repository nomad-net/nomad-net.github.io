---
lang: en
layout: page
nav: 10
---
# News

{% assign en_news_posts = site.categories.news | where: 'lang', 'en' %}
{% for post in en_news_posts %}
## {{ post.title }} <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date: "%b %d, %Y" }}</time>

{{ post.content }}
{% endfor %}
