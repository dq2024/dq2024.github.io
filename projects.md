---
layout: default
title: Your New Jekyll Site
---

<div id="projects">
  <h1>Projects</h1>
  <ul class="posts noList">
    {%- for post in site.posts -%}
      <li>
      	<span class="date">
          {%- if post.start_date and post.end_date -%}
            {{ post.start_date | date: "%b %Y" }} - {{ post.end_date | date: "%b %Y" }}
          {%- else -%}
            {{ post.date | date: "%b %Y" }}
          {%- endif -%}
        </span>
      	<h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      	<p class="description">{%- if post.description -%}{{ post.description  | strip_html | strip_newlines | truncate: 120 }}{%- else -%}{{ post.content | strip_html | strip_newlines | truncate: 120 }}{%- endif -%}</p>
      </li>
    {%- endfor -%}
  </ul>
</div>