---
layout: default
title: Project
pagination:
  enabled: true
  collection: project
  sort_reverse: true
  debug: true
---

<!-- <div class="posts">
  {% for post in paginator.posts %}
  <div class="post">
    <h1 class="post-title">
      <a href="{{ site.url }}{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>

    <span class="post-date">{{ post.date | date_to_string }}</span>

     {% if post.description.size > 140 %}{{ post.description | markdownify | remove: '<p>' | remove: '</p>' }}{% else %}{{ post.excerpt | markdownify | remove: '<p>' | remove: '</p>' }}{% endif %} <a href="{{ site.url }}{{ post.url }}" title="Read more"><strong>Read more...</strong></a>
  </div>
  {% endfor %}
</div> -->

<ol class="blog-list posts">
  {% for post in paginator.posts %}
    <!-- <li class="post post-{{ post.column }}-column"> -->
    <li class="post {% cycle 'post-2-column', 'post-1-column is-in-last-column', 'post-1-column', 'post-1-column', 'post-1-column is-in-last-column', 'post-1-column', 'post-1-column', 'post-1-column is-in-last-column' %}">
    
      <div class="post">
        <h1 class="post-title">
          <a href="{{ site.url }}{{ post.url }}">
            {{ post.title }}
          </a>
        </h1>

        <span class="post-date">{{ post.date | date_to_string }}</span>

         {% if post.description.size > 140 %}{{ post.description | markdownify | remove: '<p>' | remove: '</p>' }}{% else %}{{ post.excerpt | markdownify | remove: '<p>' | remove: '</p>' }}{% endif %} <a href="{{ site.url }}{{ post.url }}" title="Read more"><strong>Read more...</strong></a>
      </div>
    </li>

  {% endfor %}
</ol>

{% if paginator.total_pages > 1 %}
	<div class="pagination">
		{% if paginator.next_page %}
			<a class="pagination-item older" href="{{ paginator.next_page_path | prepend: site.baseurl }}">Older</a>
		{% else %}
			<span class="pagination-item older">Older</span>
		{% endif %}
		{% if paginator.previous_page %}
			<a class="pagination-item newer" href="{{ paginator.previous_page_path | prepend: site.baseurl }}">Newer</a>
		{% else %}
			<span class="pagination-item newer">Newer</span>
		{% endif %}
	</div>
{% endif %}
