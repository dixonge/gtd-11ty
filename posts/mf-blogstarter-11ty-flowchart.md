---
eleventyNavigation:
  parent: Misc
  key: mf-blogstarter Eleventy Starter Flowchart
author: Glenn Dixon
layout: layouts/home.njk
date: 2020-04-25T06:10:35+00:00
categories:
  - Misc
tags:
  - posts
---
<script async src="https://unpkg.com/mermaid@8.5.0/dist/mermaid.min.js"></script>
<script>mermaid.initialize({startOnLoad:true});</script>

Flowchart for [mf-blogstarter for Eleventy](https://github.com/marcfilleul/mf-blogstarter):

<div class="overflow-visible mermaid">
graph LR
site[metadata - _data/site.js]-->head[components/head.njk] & footer["components/footer.njk"]-->base[layouts/base.njk]
app["_css/app.css"]-->postcss[postcss] & tailwind[TailwindCSS] & purge[purgecss] & cssnano[cssnano]-->min["css/style.min.css"]-->base
classes[_data/classes.js]-->tailwind
navigation[_data/navigation.js]-->navbar[components/navbar.njk]-->header["components/header.njk"]-->base
md[Markdown files]-->post["layouts/post.njk"]-->contents(contents)-->base
</div>

