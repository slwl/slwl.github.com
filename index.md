---
layout: page
title: 好记性不如记事本 - PT8.ORG
tagline: Supporting tagline
---
{% include JB/setup %}
<ul>
{% for post in site.posts %}
<li>
<div class="posts">
<div class="post-author">
<img class="img-circle" src="{{ ASSET_PATH }}twime/images/gravatar.jpeg" /> <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
</div>
<div class="post-entry">
<span class="date pull-right">{{ post.date | date:"%Y-%m-%d" }}</span>
{% unless post.tags == empty %}   
<br /> 
<span class="tag pull-right">
{% assign tags_list = post.tags %}
{% include JB/tags_list %}
</span>	
{% endunless %}  
</div>
</div>
</li>
<hr>
{% endfor %}
<small><a class="moreposts pull-right" href="{{ BASE_PATH }}/archive.html" title="More">更多文章</a></small>
</ul>



