---
layout: default
---

{% include microblog_header.html %}

<article class="post h-entry">

<p class="e-content microblog">{{ page.content }}</p>

        <p class="post-meta">
          <time class="dt-published" datetime="{{ page.date | date_to_xmlschema }}" itemprop="datePublished">
          {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y at %I:%M%P" -%}
          {{ page.date | date: date_format }}
          </time>
          {%- if page.author -%}
          • <span itemprop="author" itemscope itemtype="http://schema.org/Person"><span class="p-author h-card" itemprop="name">{{ page.author }}</span></span>
        {%- endif -%}
        </p>

<a class="u-url" href="{{ page.url | relative_url }}" hidden></a>
</article>

{% include microblog_footer.html %}