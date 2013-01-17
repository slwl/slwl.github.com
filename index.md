---
layout: page
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}



<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% unless post.tags == empty %}
    
    <div class="tab">
		<ul class="clearfix">
		    {% assign tags_list = post.tags %}
		    {% include JB/tags_list %}
	    </ul>
	</div>
	<div class="clearfix"></div>
  {% endunless %}  
  {% endfor %}
</ul>



