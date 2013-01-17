---
layout: page
---
{% include JB/setup %}
{% for post in site.posts %}
<div class="span4">
    <h2><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.date | date_to_string }}</p>
</div><!--/span-->
{% endfor %}




