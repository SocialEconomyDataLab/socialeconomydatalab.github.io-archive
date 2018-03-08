# Social Economy Data Lab

Built using Jekyll

```bash
gem install jekyll
git clone https://github.com/SocialEconomyDataLab/socialeconomydatalab.github.io.git
cd socialeconomydatalab.github.io
bundle exec jekyll build
bundle exec jekyll serve
```

## Contributing blog posts

Blog posts should be included as Markdown files (.md) in the [\_posts/blog](/tree/master/_posts/blog) directory.

The following front-matter is necessary at the top of the file:

```yaml
---
layout: post
title:  Blog post title
date:   2018-03-06 12:00:00 +0100
category: blog
author: Author Name
excerpt: Optional custom excerpt to show on the blog post list page
---
```
1. Go to [\_posts/blog](https://github.com/SocialEconomyDataLab/socialeconomydatalab.github.io/tree/master/_posts/blog) and click on _'Create new file'_ (you need a Github account).
2. Name the file in the format ```yyyy-mm-dd-title-of-your-blog.md```
3. Copy and paste in the above front-matter (including the `---`s) and edit the `title`, `date`, `author` and `except` variables as appropriate (leave `layout` and `category` as they are).
4. Continue writing your blog post below the `---` break in [Markdown](https://daringfireball.net/projects/markdown/syntax)
5. When complete, you save the file by clicking '_Propose new file_' towards the bottom of the page.
6. Then, you need to click on the '_Create pull request_' button, and then create the pull request.
7. Someone with full access to the project will review and merge the blog post, at which point it will become live.
