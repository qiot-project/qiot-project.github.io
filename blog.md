---
layout: page
title: Blog
permalink: /blog/
---
<div class="home">
	<h2 class="post-list-heading">Posts</h2>
	<ul class="post-list">
		{% for post in site.posts %}
		<li>
			<span class="post-meta">{{ post.date | date: "%-d %B %Y" }}</span>
			<h3>
				<a class="post-link" href="{{ posts.url }}">{{ posts.title }} </a>
			</h3>
			<p>{{ posts.content}}
		</li>
		{% endfor %}
	</ul>
</div>