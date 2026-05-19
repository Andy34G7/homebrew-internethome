---
layout: base.njk
title: Homebrew Webring
---

# Homebrew Webring

Welcome to the Homebrew Webring! This is a collection of FOSS communities and sites dedicated to open source software and knowledge sharing.

## What is a Webring?

A webring is a collection of websites linked together in a circular structure, allowing visitors to navigate from one site to the next. It's a way to discover and explore related communities and projects.

## Sites in the Ring

{%- for site in sites.ring %}
**{{ site.title }}** | [{{ site.url }}]({{ site.url }})
{%- if site.blog and site.blog.length > 0 %}
{%- for feed in site.blog %} | [{{ feed.title }}]({{ feed.url }}){% endfor %}
{%- else %} | No blog feeds
{%- endif %}

{% endfor %}


## Want to Join the Webring?

To add your site to the Homebrew Webring, please:

1. Make sure your site focuses on tech, knowledge sharing and open source technologies
2. Add the webring navigation links to your footer
3. [Open a PR](https://github.com/homebrew-ec-foss/homebrew-internethome/) to request inclusion

Here's a snippet you can add to your footer HTML:

```html
<div class="webring-section">
  <div class="webring-header">
    <h3><a href="https://homebrew.hsp-ec.xyz/webring">Homebrew Webring</a></h3>
  </div>
  <div class="webring-nav">
    <a href="https://homebrew.hsp-ec.xyz/ring/prev?site=YOUR_SITE_URL" class="webring-link">← Previous</a>
    <a href="https://homebrew.hsp-ec.xyz/ring/random?site=YOUR_SITE_URL" class="webring-link">🔀 Random</a>
    <a href="https://homebrew.hsp-ec.xyz/ring/next?site=YOUR_SITE_URL" class="webring-link">Next →</a>
  </div>
</div>
```

Replace `YOUR_SITE_URL` with your website's URL (e.g., `https://yoursite.com`).


The webring helps create a community of like-minded developers and enthusiasts sharing their knowledge and passion for open source.


