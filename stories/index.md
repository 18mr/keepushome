---
layout: page
title: 'Our Stories'
permalink: /stories/
---

<ul class="post-list">
    {% for post in site.posts %}
      <li>
		<img class="featured-slider" src="{{ post.featured-image }}" />
		<div class="overlay">
			<h2>
				<a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
			</h2>
			<span>{{ post.blurb | truncatewords: 25, '...' }} <a href="{{ post.url | prepend: site.baseurl }}">Read More</a></span>
		</div>
      </li>
    {% endfor %}
</ul>