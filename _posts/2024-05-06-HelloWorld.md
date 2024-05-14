---
layout: blog-post
author: DeeJay
authorURL: https://github.com/dofddesign
title: Hello, World!
excerpt: More to come! You better watch out!
date: 2024-05-05 00:00:00 Etc/UTC
pinned: true
keywords: hello
category: Words
---
<div>
<br>Watch this space for cool things and neat stuff! Or don't, whatever.
<br>This site is hosted on GitHub, and powered by <a href="https://jekyllrb.com/" target="_blank">Jekyll</a>! Check out the repository <a href="https://github.com/dofddesign/site" target="_blank">here</a>.
</div>
{% if site.github.public_repositories %}
<br>Want to know what else I'm working on? Here's a list of my other public repositories:
{% for repository in site.github.public_repositories %}
<br>[{{ repository.name }}]({{ repository.html_url }})
<br>Primary Language: {{ repository.language }}
<br><i>{{ repository.description }}</i>
{% endfor %}
{% endif %}
