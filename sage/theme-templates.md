---
ID: 6136
post_title: Theme Templates
author: Ben Word
post_date: 2015-09-01 19:12:53
post_excerpt: ""
layout: doc
permalink: >
  https://roots.io/sage/docs/theme-templates/
published: true
docs_project:
  - 'a:1:{i:0;s:2:"17";}'
publish_to_discourse:
  - 'a:1:{i:0;s:18:"a:1:{i:0;s:1:"0";}";}'
---
The markup in Sage is based on [HTML5 Boilerplate](http://html5boilerplate.com/) with ARIA roles for accessibility and the hNews microformat for posts.

The theme root contains files that you can further extend with the normal [WordPress Template Hierarchy](http://codex.wordpress.org/Template_Hierarchy):

<dl class="dl-horizontal">
  <dt><code>404.php</code></dt>
  <dd>Error 404 page</dd>
</dl>
<dl class="dl-horizontal">
  <dt><code>base.php</code></dt>
  <dd>The <a href="/sage/docs/theme-wrapper/">theme wrapper</a> which wraps the base markup around all template files</dd>
</dl>
<dl class="dl-horizontal">
  <dt><code>index.php</code></dt>
  <dd>Archive page (used by blog page, category archives, author archives and more)</dd>
</dl>
<dl class="dl-horizontal">
  <dt><code>page.php</code></dt>
  <dd>Single page</dd>
</dl>
<dl class="dl-horizontal">
  <dt><code>single.php</code></dt>
  <dd>Single post page</dd>
</dl>
<dl class="dl-horizontal">
  <dt><code>template-custom.php</code></dt>
  <dd>An example single page template</dd>
</dl>

<p>These files include templates from the <code>templates/</code> directory which is where you&rsquo;ll be making most of your customizations:</p>
<dl class="dl-horizontal">
  <dt><code>comments.php</code></dt>
  <dd>Markup for comments</dd>
</dl>
<dl class="dl-horizontal">
  <dt><code>content-page.php</code></dt>
  <dd>Markup included from <code>page.php</code></dd>
</dl>
<dl class="dl-horizontal">
  <dt><code>content-single.php</code></dt>
  <dd>Markup included from <code>single.php</code></dd>
</dl>
<dl class="dl-horizontal">
  <dt><code>content.php</code></dt>
  <dd>Markup included from <code>index.php</code></dd>
</dl>
<dl class="dl-horizontal">
  <dt><code>entry-meta.php</code></dt>
  <dd>Post entry meta information included from <code>content-single.php</code></dd>
</dl>
<dl class="dl-horizontal">
  <dt><code>footer.php</code></dt>
  <dd>Footer markup included from <code>base.php</code></dd>
</dl>
<dl class="dl-horizontal">
  <dt><code>head.php</code></dt>
  <dd><code>&lt;head&gt;</code> markup included from <code>base.php</code></dd>
</dl>
<dl class="dl-horizontal">
  <dt><code>header.php</code></dt>
  <dd>Header markup included from <code>base.php</code></dd>
</dl>
<dl class="dl-horizontal">
  <dt><code>page-header.php</code></dt>
  <dd>Page title markup included from most of the files in the theme root</dd>
</dl>
<dl class="dl-horizontal">
  <dt><code>sidebar.php</code></dt>
  <dd>Sidebar markup included from <code>base.php</code></dd>
</dl>

## Extending templates

Even with the [theme wrapper](/sage/docs/theme-wrapper/), the normal [WordPress Template Hierarchy](http://codex.wordpress.org/Template_Hierarchy) is still intact. Here’s some examples:

* Copy `index.php` to `author.php` for customizing author archives
* Copy `index.php` to `home.php` for customizing the Home page if you’re showing the latest posts (under Reading Settings) instead of a static front page
* Copy `index.php` to `archive-gallery.php` for customizing the archive page for a custom post type registered as `gallery`
* Copy `page.php` to `front-page.php` for customizing the static front page
* Copy `page.php` to `page-about.php` for customizing a page called About

The [theme wrapper documentation](/sage/docs/theme-wrapper/) goes into depth about creating new `base.php` files, but if you’d like to have a customized `base.php` based on a certain template, just copy it to `base-<template name>.php`. You can add conditional statements to `base.php` whenever possible and should generally aim to not have multiple theme wrappers in your theme.