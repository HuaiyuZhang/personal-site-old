---
layout: post
title: Use Blogdown to Build Site
---


## Set up for blogdown

Create a new rmarkdown file, it automatically install several packages.

```R
if (!requireNamespace("devtools")) install.packages("devtools")
devtools::install_github("rstudio/blogdown")
blogdown::install_hugo()
# Specify any theme you want.Google “hugo themes". Use 'universal' as example.
blogdown::new_site(theme = "devcows/hugo-universal-theme") 
```

The site is ready then.

Now if we close the browser, and want to look at it again, go to 'addins->serve site'. After installing several packages, the site shows again. We can change the 'content' folder for the materials. They are written in markdown. And modify 'config.toml' for the styles. See https://themes.gohugo.io/hugo-universal-theme/ for details.

If we want to add a new post, still, we can use the 'addins-> New post'.

## How to use git under rstudio

https://www.r-bloggers.com/rstudio-and-github/

If we need to push something new, commit all and use tool->shell:

```R
git push -u origin master
```
