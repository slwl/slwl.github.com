---
layout: page
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}
<ul class="posts word-wrap">
{% for post in site.posts %}
<li>
<div class="post-author">
<img class="img-circle" src="https://secure.gravatar.com/avatar/3b00ffdc531cc40c9f6dad3ab104b208?s=32&d=https://a248.e.akamai.net/assets.github.com%2Fimages%2Fgravatars%2Fgravatar-user-32.png" /> <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
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
</li>
<hr>
{% endfor %}
<small><a class="moreposts" href="{{ BASE_PATH }}/archive.html" title="More">更多文章</a></small>
</ul>



