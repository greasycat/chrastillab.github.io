---
layout: default
title: How to setup a github page site with Jekyll like this site
nav_order: 1
parent: GitHub Page
---
# What is Jekyll

Jekyll is a popular open-source static site generator (SSG) written in Ruby. It's designed to simplify the process of creating and maintaining websites, particularly blogs and simple websites. Jekyll takes your content, written in plain text or in Markdown, and combines it with templates to generate static HTML pages.



# Perquisite (For Windows Users)
1. Installing Ruby with Bundler
	1. Go to [Ruby Installer Download](https://rubyinstaller.org/downloads/)
	2. Download the latest release **with** DevKit (DevKits allows the installation of jekyll)
			- At the end of the installation, check the box to install `MSYS2 and MINGW`
	3. Open a command shell to check ruby is installed `ruby --vesion`
		- If command is not found or recognized, check that the `PATH` environment variables contains path to ruby executable and restart command shell
	4. Run `gem install jekyll bundler`
	5. Sip coffee (2-5 minutes depends on your computer specs)

2. Follow [Detailed GitHub Official Tutorial](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll)
	1. Ensure you've commented out  the line that starts with `gem "jekyll"` in `Gemfile`
	2. Ensure you've added `gem "github-pages", "~> GITHUB-PAGES-VERSION", group: :jekyll_plugins` and replace the version accordingly

### A sample `_config.yml`
```yml
# Title of the website
title: Chrastil Lab Documentation

# Email (can be removed)
email: spatialneuroscience@uci.edu

# Some decription
description: Welcome to the Chrastil Lab Code Documentation Repository on GitHub! This repository serves as the central hub for organizing and sharing the coding documentation related to the research and projects conducted by the Chrastil Lab.

# Do not change unless you're not using gh page
baseurl: "/" 

# The link to the website
url: "http://chrastillab.github.io/"

# A theme-related variable to put a github link on the footer
github_username: spatialneuroscience

# Choose a Theme
theme: minima

# Plugins
plugins:
  - jekyll-feed
```

# Changing the theme
Jekyll has a lively community that creates various themes for different needs. This makes it simple to discover a theme you prefer and use it for your own project. For our current lab documentation site, I chose the [Just The Docs](https://just-the-docs.com/) theme. It's a straightforward theme that's great for organizing content effectively.

### Installing the theme

1. Add a new line `gem "just-the-docs"` to `Gemfile`
2. Editing the `_config.yml`

### Changing `_config.yml` (read the comments)

```yml
# Changing from minima to just-the-docs
theme: just-the-docs

# The logo image on the top left
logo: "/assets/images/logo.png"

# The icon on the browser tab
favicon_ico: "/assets/images/brainnn.png"

# An engine to plot diagrams
mermaid:
  version: "9.1.3"

# Links to be displayed on the top navigation bar 
aux_links:
  "Chrastil Lab Github":
    - "//github.com/chrastillab"
  "Spatial Neuroscience Github":
    - "//github.com/chrastillab"

# Make sure when people click on the link, it will opne a new page
aux_links_new_tab: true

# Defining Custom collection that can be shown on left sidebar
collections:
  misc:
    permalink: "/:collection/:path/"
    output: true

# Pass the collection information to the theme variable
just_the_docs:
  collections:
    misc:
      name: Miscellaneous
```

3. Run `bundle install`
4. Run `bundle exec jekyll serve` to test the changes
5. Git push your changes

There're a lot more customizations that could be enabled but we will omit them here. Check out the [configuration](https://just-the-docs.com/docs/configuration/) yourself!

# Theme not properly showing on Github Pages

Open the github repo -> Settings -> Pages -> Build and Deployment -> Github Action
- Search for a github action called `Jekyll` created by Github Action
- Click configure and don't change anything, the workflow should automatically build and depoly the site (if you put your source code in a subfolder, you should move them to the root folder or finding another GitHub Action)
