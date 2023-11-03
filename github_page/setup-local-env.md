---
layout: default
title: 1. Set Up Local Environment
nav_order: 1
parent: Write Your Own Documentation!
---
{: .note}
This is  a copy-paste of the repo readme file [REAME](https://github.com/ChrastilLab/chrastillab.github.io)

## Accessing the Documentation Locally


To view and edit the documentation locally on your computer, you will need to set up a local development environment using Jekyll, which is a popular static site generator. Follow the steps below to get started:

### Prerequisites

What you need
- Ruby
- RubyGem
- Bundler

### Install Prerequisites

Read the official installation guide [Jekyll official Installation Guide](https://jekyllrb.com/docs/installation/). It will guide your installation of Ruby and RubyGem step-by-step
-  If **Bundler** is not installed after finishing the above guide: Install Bundler by running `gem install bundler` in your terminal.

### Setting Up the Local Environment

1. Clone this repository to your local machine using the following command:

   ```
   git clone https://github.com/chrastillab/chrastillab.github.io
   ```

2. Navigate to the repository's root directory:

   ```
   cd chrastillab.github.io
   ```

3. Install the required dependencies using Bundler:

   ```
   bundle install
   ```

### Viewing the Documentation

1. Once the dependencies are installed, you can start a local development server by running the following command:

   ```
   bundle exec jekyll serve
   ```

2. Open your web browser and visit the following URL:

   [http://127.0.0.1:4000](http://127.0.0.1:4000)

   You should see the documentation website running locally.

### Editing the Documentation

1. To make changes to the documentation, navigate to the appropriate Markdown files in the repository's directory structure.

2. Edit the Markdown files using your preferred text editor.

3. Save your changes.

4. Refresh the documentation website in your browser to see your edits.