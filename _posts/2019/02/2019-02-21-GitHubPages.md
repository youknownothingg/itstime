---
layout: post
title: GitHub Pages & Jekyll
lang: zh
category: Util
---
#### reference
* [How to build a GitHub Pages](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/)
* [Jekyll Doc Theme](https://idratherbewriting.com/documentation-theme-jekyll/index.html)
* [Jekyll theme-cn1](https://jekyllcn.com/)
* [Jekyll theme-cn2](https://www.jekyll.com.cn/)

#### getting started
* install ruby & jekyll (on windows)

```
# install ruby
choco install ruby -y
gem install bundler

# install jekyll
gem install jekyll

# specify version
gem install jekyll -v '2.0.0.alpha.1'
```

* upgrade jekyll

```
jekyll --version
gem list jekyll
gem outdated
gem search jekyll --remote
gem update jekyll
```

* create jekyll site

```
# create a new project
jekyll new myblog

# boot a local server
cd myblog
jekyll serve
# => Now browse to http://localhost:4000
# specify version
jekyll serve -p 1234
```

* for GitHub Pages: new Gemfile file under root

```
source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins
```

* Install Jekyll and other dependencies from the GitHub Pages gem

```
bundle install
```

* Build your local Jekyll site

```
bundle exec jekyll serve
```

* access the site

> Keeping your site up to date with the GitHub Pages gem

```
Jekyll is an active open source project and is updated frequently. As the GitHub Pages server is updated, the software on your computer may become out of date, resulting in your site appearing different locally from how it looks when published on GitHub.

1. Open Git Bash.

2. Run this update command:

    If you followed our setup recommendations and installed Bundler, run bundle update github-pages or simply bundle update and all your gems will update to the latest versions.

    If you don't have Bundler installed, run gem update github-pages
```
