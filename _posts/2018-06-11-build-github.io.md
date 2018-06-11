---
layout: post
title: Build github.io
---

1. Create a new repo called username.github.io

2. JekyII is automatically incorporated into github site. In the setting for the repo, there is a way of choosing the theme.

   >  QUICK REMINDER FOR GIT
   >
   >  git add -A
   >
   >  git commit -m 'message'
   >
   >  git push -u origin master
   >
   >  git pull

3. Once the theme is chosen,  `_config.yml` will be shown in the repo. Edit  it with some information. For example

   ```yml
   highlighter: Randomania
   name: Huaiyu's website
   description: Collecting ideas in statistics
   url: "https://huaiyuzhang.github.io"

   markdown: kramdown
   theme: jekyll-theme-minimal #activate the theme
   ```

4. Now the website should be fine.

5. Add new folders that you need
See [this](https://github.com/jekyll/minima#customization)

## Locally hosting (not necessary)：


[guide](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/)

1. To manage the site locally, it is recommended to use local JekyII
2. Download `ruby` for supporting `bundler` for `JekyII`.

