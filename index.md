---
layout: page
---
{% include JB/setup %}
<div class="span6">
{% for post in site.posts %}

    <h4><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h4>
    <p>{{ post.date | date_to_string }}</p>

{% endfor %}

</div><!--/span-->


