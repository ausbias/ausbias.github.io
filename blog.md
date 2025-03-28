---
layout: default
title: Blog
---
<style>
@font-face {
  font-family: 'Oswald';
  src: url('/assets/fonts/oswald-regular.ttf') format('truetype');
}

h1, h2, h3, h4, h5, h6,
.site-title,
.site-nav,
.site-nav a {
  font-family: 'Oswald', sans-serif !important;
}
</style>


<h1>Blog</h1>

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small> – {{ post.date | date: "%B %d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
