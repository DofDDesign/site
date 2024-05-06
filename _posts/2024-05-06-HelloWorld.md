---
layout: blog-post
author: DeeJay
authorURL: https://github.com/dofddesign
title: Hello, World!
excerpt: More to come! You better watch out!
date: 2024-05-05 00:00:00 +0000
pinned: true
---
Watch this space for cool things and neat stuff! Or don't, whatever.
<br>This site is hosted on GitHub, and powered by <a href="https://jekyllrb.com/" target="_blank"><u>Jekyll</u></a>! Check out the repository <a href="https://github.com/dofddesign/site" target="_blank"><u>here</u></a>.

<br>Want to know what else I'm working on? Here's a list of my other public repositories:
{% for repository in site.github.public_repositories %}
<br>[{{ repository.name }}]({{ repository.html_url }})
{% endfor %}
