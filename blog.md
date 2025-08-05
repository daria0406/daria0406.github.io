---
layout: page
title: Blog
permalink: /blog/
---

# Blog

Thoughts, insights, and commentary on topics in my field and beyond.

---

<div class="home">
  {%- if site.posts.size > 0 -%}
    <ul class="post-list">
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
      {%- for post in site.posts -%}
      <li>
        <span class="post-meta">{{ post.date | date: date_format }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        {%- if site.show_excerpts -%}
          {{ post.excerpt }}
        {%- endif -%}
      </li>
      {%- endfor -%}
    </ul>

  
  {%- else -%}
    <p>No blog posts yet. Check back soon for updates!</p>
  {%- endif -%}
</div>