---
layout: default
---

{% for post in site.posts limit: 10 %}
	<h1>{{ post.title }}</h1>
	<p><i>{{ post.date | date_to_long_string }}</i></p>
	{{ post.excerpt }}
	<p>
	  <a href="{{ post.url }}">Read >></a>
	</p>
	<hr>
{% endfor %}