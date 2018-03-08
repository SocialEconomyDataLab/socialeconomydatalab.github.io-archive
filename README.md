# Social Economy Data Lab

Built using Jekyll

```
gem install jekyll
git clone https://github.com/SocialEconomyDataLab/socialeconomydatalab.github.io.git
cd socialeconomydatalab.github.io
bundle exec jekyll build
bundle exec jekyll serve
```

## Writing blog posts

Blog posts should be included as Markdown files (.md) in the [\_posts/blog](/tree/master/_posts/blog) directory.

The following front-matter is necessary:

```yaml
---
layout: post
title:  Blog post title
date:   2018-03-06 12:00:00 +0100
category: blog
author: Author Name
excerpt: Custom excerpt to show on the blog post list pagea
---
```
