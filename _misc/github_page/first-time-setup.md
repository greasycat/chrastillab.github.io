---
layout: default
title: How to setup a github page site with Jekyll like this site
nav_order: 1
parent: GitHub Page
---
# Perquisite (For Windows Users)

1. Installing Ruby with Bundler
	1. Go to [Ruby Installer Download](https://rubyinstaller.org/downloads/)
	2. Download the latest release **with** DevKit (DevKits allows the installation of jekyll)
			- At the end of the installation, check the box to install `MSYS2 and MINGW`
	3. Open a command shell to check ruby is installed `ruby --vesion`
		- If command is not found or recognized, check that the `PATH` environment variables contains path to ruby executable and restart command shell
	4. Then, run `gem install jekyll bundler`
	5. Sip coffee (2-5 minutes depends on your computer specs)

2. Follow [Detailed GitHub Official Tutorial](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll)
	1. Ensure you've commented out  the line that starts with `gem "jekyll"` in `Gemfile`
	2. Ensure you've added `gem "github-pages", "~> GITHUB-PAGES-VERSION", group: :jekyll_plugins` and replace the version accordingly

## The `_config.yml`
```yml
title: Chrastil Lab Documentation on GitHub Page
email: spatialneuroscience@uci.edu
description: Welcome to the Chrastil Lab Code Documentation Repository on GitHub! This repository serves as the central hub for organizing and sharing the coding documentation related to the research and projects conducted by the Chrastil Lab.
baseurl: "/" 
url: "http://chrastillab.github.io/" 
github_username: spatialneuroscience, chrastillab
# Build settings
theme: minima
plugins:
  - jekyll-feed
```
