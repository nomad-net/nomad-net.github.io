---
lang: ru
layout: page
nav: 10
---
# Новости

{% assign ru_news_posts = site.categories.news | where: 'lang', 'ru' %}
{% for post in ru_news_posts %}
## {{ post.title }} <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date: "%b %d, %Y" }}</time>

{{ post.content }}
{% endfor %}