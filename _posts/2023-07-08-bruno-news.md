---
layout: post
title: Bruno News
author: Bruno Zhong
---

Bruno News is a news feed that can show Bruno's interests and other Bruno-related stuff.

## Why read Bruno News?

Some reasons include:

### Bruno News supports code highlighting.

You can see plain old HTML:

```html
<style>
  body {
    font: sans-serif;
  }
</style
<h1>Plain old HTML</h1>
<p>With a script and some styles.</p>
<script>
  alert("Hi!")
</script>
```

Or also "Liquid", the stuff that builds this news feed.

{% raw %}
```liquid
<ol>
  {% for post in site.posts %}
    <p>See {{ post.title }}!</p>
  {% endfor %}
</ol>
```
{% endraw %}
