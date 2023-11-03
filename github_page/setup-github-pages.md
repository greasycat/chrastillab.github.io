---
layout: default
title: (HowTo) Setup a Github Page with Jekyll
parent: Write Your Own Documentation!

---
{: .warning } 
This is a tutorial for people who want to create their own github page

# What is Jekyll

Jekyll is a popular open-source static site generator (SSG) written in Ruby. It's designed to simplify the process of creating and maintaining websites, particularly blogs and simple websites. Jekyll takes your content, written in plain text or in Markdown, and combines it with templates to generate static HTML pages.



# Installation
## Installing Ruby with Bundler  (For Windows only)
 
1. Visit the [Ruby Installer Download](https://rubyinstaller.org/downloads/) webpage.

2. Download the most recent release of Ruby, ensuring that it includes the DevKit. The DevKit is necessary for Jekyll installation.

   - During the installation process, be sure to check the box to install `MSYS2 and MINGW`.

3. Open a command shell to verify that Ruby has been successfully installed by entering the following command:

   ```shell
   ruby --version
   ```

   - If the command is not found or not recognized, please check that the `PATH` environment variable includes the path to the Ruby executable. After making this adjustment, restart the command shell.

These refined instructions should help users install Ruby and the necessary components for Jekyll more effectively. If you have any further instructions or text that you'd like me to refine, please feel free to share them.
 
## Install Jekyll and Bundle
1. Execute the following command to install Jekyll and Bundler:

   ```shell
   gem install jekyll bundler
   ```

2. Take a moment to enjoy a cup of coffee while the installation process runs. The duration may vary from 2 to 5 minutes, depending on your computer's specifications.

These instructions are now concise and clear, making it easy for users to install Jekyll and Bundler with a brief coffee break. If you have any more text that needs refinement or further assistance, feel free to share it.

## Configuring Jekyll
### Option 1: Use the GitHub Page Gem
This gem simplifies the setup process by providing all the necessary components, including themes and plugins, with minimal configuration required. Follow these steps:

1. You can refer to the [Detailed GitHub Official Tutorial](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll) for comprehensive guidance.

2. In your project's `Gemfile`, make sure to comment out the line that starts with `gem "jekyll"`.

3. Add the following line to your `Gemfile`, replacing `GITHUB-PAGES-VERSION` with the desired version:

   ```ruby
   gem "github-pages", "~> GITHUB-PAGES-VERSION", group: :jekyll_plugins
   ```

**Sample `_config.yml` file:**

```yaml
# Website Title
title: Chrastil Lab Documentation

# Email (optional)
email: spatialneuroscience@uci.edu

# Description
description: Welcome to the Chrastil Lab Code Documentation Repository on GitHub! This repository serves as the central hub for organizing and sharing coding documentation related to research and projects conducted by the Chrastil Lab.

# Do not change unless you're not using a GitHub page
baseurl: "/"

# Website URL
url: "http://chrastillab.github.io/"

# GitHub Username (for theme-related footer link)
github_username: spatialneuroscience

# Choose a Theme
theme: minima

# Plugins
plugins:
  - jekyll-feed
```

These refined instructions and sample configuration should help users set up their GitHub Pages site with Jekyll more smoothly. If you have any further text or instructions that require refinement, please let me know.

### Option 2: Use vanilla Jekyll
I personally find the GitHub Pages Gem a bit cumbersome for my needs. Therefore, for Lab Documentation, I've chosen to use vanilla Jekyll. The advantages are clear: it offers a faster site building process and allows you to easily add any necessary plugins later on.

To set up your documentation site using vanilla Jekyll, follow these steps:

1. Start by creating an empty GitHub repository (there's no need to add a readme at this point).

2. Clone the repository to your local machine and navigate to its directory using the command line.

3. (Optional) If you want to use the `gh-pages` branch for your GitHub Pages site, create a new branch named `gh-pages`. This step is optional but can help keep your main branch clean.

4. Run the following command to generate the basic Jekyll structure: 

   ```shell
   jekyll new --skip-bundle
   ```

   This command will create the necessary files and directories, including the `Gemfile` and default configurations.

5. Open the `Gemfile` in your favorite text editor and add any additional Jekyll plugins you require. Be sure to specify the version of each plugin if needed.

6. Install the bundled gems by running:

   ```shell
   bundle install
   ```

   This command will download and install the specified Jekyll plugins and dependencies.

7. Add the plugins to the `_config.yml` like the sample code below

7. To preview your site locally, run the following command:

   ```shell
   bundle exec jekyll serve
   ```

   This will start a local development server, and you can access your Jekyll site in your web browser at the specified address (usually at [localhost:4000](http://localhost:4000)).
   
{: .highlight }
The theme have not been set yet, so the page may look horrible

By following these steps, you can set up your Lab Documentation site with vanilla Jekyll, enjoy faster site building times, and have the flexibility to add plugins as needed.

**Sample `_config.yml` file:**
```yml
title: Chrastil Lab Documentation
baseurl: "/" # the subpath of your site, e.g. /blog
url: "http://chrastillab.github.io/" # the base hostname & protocol for your site, e.g. http://example.com

plugins:
  - jekyll-redirect-from
  - jekyll-relative-links
  - jekyll-sitemap
  - jekyll-seo-tag
```

**Sample `Gemfile` file**
```ruby
source "https://rubygems.org"

gem "jekyll", "~> 4.3.2"
gem 'jekyll-redirect-from'
gem 'jekyll-relative-links'
gem 'jekyll-sitemap'
gem 'jekyll-seo-tag'

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem
# do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
gem "webrick", "~> 1.8"
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
  "Chrastil Lab Github": "//github.com/chrastillab"
  "Spatial Neuroscience Github": "//github.com/chrastillab"

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
