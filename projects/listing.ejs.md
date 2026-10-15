<% /* Quarto 1.10: <%- escapes HTML (including attributes).
      item.path and item.image are resolved by Quarto; its HTML processor
      makes project-root paths relative to this page for subdirectory hosting.
      Explicit descriptions are required; keep their content as plain text. */ %>
```{=html}
<div class="list project-catalog">
<% for (const item of items) { %>
<article class="project-entry" <%= metadataAttrs(item) %>>
<div class="project-entry-copy">
<h2 class="listing-title no-anchor"><a class="no-external" href="<%- item.path %>"><%- item.title %></a></h2>
<p class="listing-description"><%- item.description %></p>
<% if (item.categories && item.categories.length) { %>
<ul class="project-tags" aria-label="Categorías">
<% for (const category of item.categories) { %>
<li class="listing-category"><%- category %></li>
<% } %>
</ul>
<% } %>
</div>
<% if (item.image) { %>
<div class="project-thumbnail"><img src="<%- item.image %>" alt="<%- item['image-alt'] || '' %>" loading="lazy"></div>
<% } %>
</article>
<% } %>
</div>
```
