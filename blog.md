---
layout: page
title: Blog
permalink: /blog/
---
<div class="home">
	<ul class="post-list">
		{% for post in site.posts %}
		<li>
			<span class="post-meta">{{ post.date | date: "%-d %B %Y" }}</span>
			<h3>
				<a class="post-link" href="{{ post.url }}">{{ post.title }} </a>
			</h3>
			<p>{{ post.content}}
		</li>
		{% endfor %}
	</ul>
</div>