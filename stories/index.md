---
layout: page
title: 'Our Stories'
permalink: /stories/
---

<script src="{{ baseurl }}/static/js/plugins/jquery.fitvids.js"></script>
<script>
	$(document).ready(function(){
		// Target your .container, .wrapper, .post, etc.
		$(".video").fitVids();
	});
</script>

<ul class="post-list">
    {% for post in site.posts %}
      <li>
	    {% if post.video-url %}
		<div class="video">
		<iframe src="{{ post.video-url }}" allowfullscreen></iframe>
		</div>
		<div class="vid-caption">
			<h2>
				<a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
			</h2>
			<span>{{ post.blurb | truncatewords: 25, '...' }} <a href="{{ post.url | prepend: site.baseurl }}">Read More</a></span>
		</div>
		{% else %}
		<img class="featured" src="{{ post.featured-image }}" />
		<div class="overlay">
			<h2>
				<a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
			</h2>
			<span>{{ post.blurb | truncatewords: 25, '...' }} <a href="{{ post.url | prepend: site.baseurl }}">Read More</a></span>
		</div>
		{% endif %}
      </li>
    {% endfor %}
</ul>