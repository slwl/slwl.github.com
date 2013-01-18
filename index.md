---
layout: page
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}
<ul>
{% for post in site.posts %}
<li><img src="https://secure.gravatar.com/avatar/3b00ffdc531cc40c9f6dad3ab104b208?s=32&d=https://a248.e.akamai.net/assets.github.com%2Fimages%2Fgravatars%2Fgravatar-user-32.png" class="img-circle"> <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a><span class="date">{{ post.date | date:"%Y-%m-%d" }}</span>
{% unless post.tags == empty %}    
<span class="tag pull-right">
{% assign tags_list = post.tags %}
{% include JB/tags_list %}
</span>	
{% endunless %}  
</li>
<hr>
{% endfor %}
<small><a class="moreposts" href="{{ BASE_PATH }}/archive.html" title="More">更多文章</a></small>
</ul>



