---
layout: page
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}



<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% unless page.tags == empty %}
    <h4>Tags</h4>
    <ul class="tag_box">
    {% assign tags_list = page.tags %}
    {% include JB/tags_list %}
    </ul>
  {% endunless %}  
  {% endfor %}
</ul>



