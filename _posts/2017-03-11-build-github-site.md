---
layout: post
title: Build github.io with Jekyll
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

[Github guide](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/)

1. To manage the site locally, it is recommended to use local JekyII
2. Download `ruby` for supporting `bundler` for `JekyII`.
```
jekyll serve
```

## MathJax
[This](https://lyk6756.github.io/2016/11/25/write_latex_equations.html) eventually works.
Only Kramdown works with Github.

In-line equation uses `$$math_expression$$` to quote. Separate line display can also use `$$math_expression$$` in a new line.


## Images
Adding images is a step easy to get error. Some points to pay attention: the spell is case sensitive; forward slash; path.

My path always has error, [this solution](http://sgeos.github.io/github/jekyll/2016/08/30/adding_images_and_downloads_to_a_github_pages_jekyll_blog.html) works:

1. add `url: https://xxxxxx.github.io` to `_config.yml`

2. insert image by `![image_name]({{ site.url }}/assets/image.PNG)`. Upload the image to `assets` folder under the root.


