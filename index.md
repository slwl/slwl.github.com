---
layout: page
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}



<ul class="posts">
{% for post in site.posts %}
<li><img src="https://secure.gravatar.com/avatar/3b00ffdc531cc40c9f6dad3ab104b208?s=32&d=https://a248.e.akamai.net/assets.github.com%2Fimages%2Fgravatars%2Fgravatar-user-32.png" class="img-circle"><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
{% unless post.tags == empty %}    
<div class="tab">
{% assign tags_list = post.tags %}
{% include JB/tags_list %}
</div>	
{% endunless %}  
</li>
{% endfor %}
</ul>



