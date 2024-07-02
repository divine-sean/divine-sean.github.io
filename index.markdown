---
layout: home
---

<style>
.pinned-label {
  color: #32CD32; /* Green color */
  margin-left: 10px; /* Adjust margin as needed */
}
</style>

<!-- Display pinned posts -->
<div>
  <h1>Pinned Posts</h1>
  {% assign pinned_posts = site.posts | where: "pinned", true %}
  {% if pinned_posts.size > 0 %}
    {% for post in pinned_posts %}
      <h2><a href="{{ post.url }}">{{ post.title }}</a><span class="pinned-label">Pinned</span></h2>
    {% endfor %}
  {% else %}
    <p>No pinned posts found.</p>
  {% endif %}
</div>

