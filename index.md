---
layout: page
---
{% include JB/setup %}
{% for post in site.posts %}
<div class="span6">
    <h4><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h4>
    <p>{{ post.date | date_to_string }}</p>
</div><!--/span-->
{% endfor %}




