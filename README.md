# README for GitHub Documentation Page

Welcome to the documentation page for our GitHub repository! This repository contains documentation and information related to our project. If you would like to contribute or edit the documentation, please follow the instructions below.

## Accessing the Documentation Locally


To view and edit the documentation locally on your computer, you will need to set up a local development environment using Jekyll, which is a popular static site generator. Follow the steps below to get started:

### Prerequisites

What you need
- Ruby
- RubyGem
- Bundler

### 1. Install Prerequisites

Read the official installation guide [Jekyll official Installation Guide](https://jekyllrb.com/docs/installation/). It will guide your installation of Ruby and RubyGem step-by-step
-  If **Bundler** is not installed after finishing the above guide: Install Bundler by running `gem install bundler` in your terminal.


### 2. Fork to Your Own Repo
Click on this [Link](https://github.com/ChrastilLab/chrastillab.github.io) and find the fork button as shown in the image below
- ![forking](/assets/images/github_page/adding-documentation/fork.png)

### 3. Setting Up the Local Environment

1. Clone **your own** repository to your local machine using the following command:

{: .highlight}
remember to replace `YOUR_GITHUB_USERNAME` with your actual GitHub  username

   ```
   git clone https://github.com/YOUR_GITHUB_USERNAME/chrastillab.github.io
   ```

2. Navigate to the repository's root directory:

   ```
   cd chrastillab.github.io
   ```

3. Install the required dependencies using Bundler:

   ```
   bundle install
   ```

### 4. Viewing the Documentation

1. Once the dependencies are installed, you can start a local development server by running the following command:

   ```
   bundle exec jekyll serve
   ```

2. Open your web browser and visit the following URL:

   [http://127.0.0.1:4000](http://127.0.0.1:4000)

   You should see the documentation website running locally.

### Editing the Documentation 

Suggest reading: [How to add your own documentation](http://127.0.0.1:4000/github_page/markdown.html)

1. To make changes to the documentation, navigate to the appropriate Markdown files in the repository's directory structure.

2. Edit the Markdown files using your preferred text editor.

3. Save your changes.

4. Refresh the documentation website in your browser to see your edits.

### Contributing

If you'd like to contribute to the documentation, please fork this repository, make your changes, and then submit a pull request. We welcome contributions from the community!

For more information on how to contribute to this repository, please refer to [Add your own documentation](http://chrastillab.github.io/github_page/)

Thank you for your interest in improving our documentation! If you have any questions or encounter any issues, please feel free to open an issue on this repository or contact us through our official channels.

Happy documenting! 📚