[![Gem Version](https://badge.fury.io/rb/jekyll-sleek.svg)](https://badge.fury.io/rb/jekyll-sleek) [![Build Status](https://travis-ci.org/janczizikow/sleek.svg?branch=master)](https://travis-ci.org/janczizikow/sleek) [![license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/janczizikow/sleek)
# Sleek Template (Customized by LC WiCS)

A modern [Jekyll](https://jekyllrb.com/) theme focused on speed performance & SEO best practices.

## Features

* Compatible with [Github Pages](https://pages.github.com/)
* Minimal, responsive and speed performance optimized
* SEO friendly, with help of [Jekyll SEO Plugin](https://github.com/jekyll/jekyll-seo-tag)
* Easy [Google Tag Manager](https://tagmanager.google.com/) Integration
* Support for [Disqus](https://disqus.com/) comments
* Form submissions with [Formspree](https://formspree.io/)

[Preview Demo](https://janczizikow.github.io/sleek/)

## Installation

### System Requirements

To use this project, you'll need the following things on your local machine:

#### Jekyll

```shell
gem install jekyll
```

#### NodeJS

Download and open the [NodeJS installer](https://nodejs.org/en/)

#### Gulp.js (optional, but recommended)

```shell
sudo npm install -g gulpfile
```

### Up & Running

1. Clone or download the repo into directory of your choice: `git clone https://github.com/lehmanwics/lehmanwics.github.io.git`
2. Inside the directory run `bundle install` and `npm install`
3. If you want to use [gulp.js](https://gulpjs.com/) run `gulp` or `npm start`
  * if you don't want to use gulp you can simply run `bundle exec jekyll serve`

#### Installing to existing jekyll project

Add this line to your Jekyll site's `Gemfile`:

```ruby
gem "jekyll-sleek"
```

And add this line to your Jekyll site's `_config.yml`:

```yaml
theme: jekyll-sleek
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install jekyll-sleek


## File Structure Overview

```bash
sleek
├── _includes	                 # theme includes
├── _js	                       # javascript files (by default jquery will be included with the scripts inside)
├── _layouts                   # theme layouts (see below for details)
├── _pages                     # pages folder (empty by default)
├── _posts                     # blog posts
├── _sass                      # Sass partials
├── assets
|  ├── css	                   # minified css files  
|  ├── img                     # images and icons used for the template
|  └── js		                   # bundled and minified files from _js folder
├── _config.yml                # sample configuration
├── gulpfile.js                # gulp tasks (tasks autorunner)
├── index.md                   # sample home page (blog page)
└── package.json               # gulp tasks
```

## Usage

### Making and publishing changes to CSS files
*Only* edit CSS files in the _sass folder. 
- Once edits are made and saved, run ```jekyll serve``` to see your changes locally
- Run ```gulp sass``` from your preferred terminal or console to save the CSS file changes
- Add and commit files to repo to publish changes

### Publishing and drafting blog posts

Blog posts are saved under the *_posts* folder. To create a new blog post, create a new file in the _posts folder and configure the post as follows:
- Save the file in the following format: ``` YYY-MM-DD-title-of-blog-post.md ```
- Add the following to the beginning of the blog post file:
```
---
layout: post                                            # type of post
title: Join Us at our Interest Meeting in April!        # title of the blog post
featured-img: flyer_event--wicsinterestmeeting.png      # image used in thumbnail and header (saved in the assets/img folder)
summary: enter summary here                             # optional line - create a summary for the post
published: true											# optional line - set to false if you want to publish later
---

Text and code goes here.

```

You can use some HTML code in the blogpost, although markdown formatting is suggested. See the markdown cheatsheet blog post for a tutorial.

Once you have completed the post, run ```jekyll serve``` to see your post locally. If you are satisfied with the changes, commit and push it to the repo.

### Site configuration

TODO

### Google Tag Manager

TODO

### Disqus

To enable Disqus comments, add your [Disqus shortname](https://help.disqus.com/customer/portal/articles/466208) to `_config.yml`:

```yaml
disqus:
  shortname: my_disqus_shortname
```
### Formspree


TODO: Write usage instructions here. Describe your available layouts, includes, sass and/or assets.

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/janczizikow/sleek. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Development

To set up your environment to develop this theme, run `bundle install`.

Your theme is setup just like a normal Jekyll site! To test your theme, run `bundle exec jekyll serve` and open your browser at `http://localhost:4000`. This starts a Jekyll server using your theme. Add pages, documents, data, etc. like normal to test your theme's contents. As you make modifications to your theme and to your content, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

When your theme is released, only the files in `_layouts`, `_includes`, `_sass` and `assets` tracked with Git will be bundled.
To add a custom directory to your theme-gem, please edit the regexp in `jekyll-sleek.gemspec` accordingly.

## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
