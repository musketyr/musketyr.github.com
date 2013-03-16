---
layout: page
title: Groovy in the Clouds
tagline: Vladimír Oraný
---
{% include JB/setup %}

{% for post in site.posts limit:5 %}
<div>
    <span>{{ post.date | date_to_string }}</span>
    <h2><a href="{{post.url}}">{{ post.title }}</a></h2>
    <summary>{{ post.content }}</summary>
    <hr/>
</div>
{% endfor %}

## Find more
### Categories
<ul class="tag_box inline">
  {% assign categories_list = site.categories %}
  {% include JB/categories_list %}
</ul>

### Tags
<ul class="tag_box inline">
  {% assign tags_list = site.tags %}  
  {% include JB/tags_list %}
</ul>

### Feeds

[RSS](/rss.xml), [Atom](/atom.xml)
