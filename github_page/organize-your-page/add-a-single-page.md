---
layout: default
title: "Add a Single Page"
nav_order: 2
parent: "3. Organize your Pages"
grand_parent: Write Your Own Documentation!
---


# How to Add a Single Page

In Jekyll, creating a single page involves adding metadata at the top of the Markdown file. This metadata helps Jekyll organize the site's content. Here's a step-by-step guide on how to create a sample page called `single.md` in the root of your project folder:

1. **Create the Markdown File**: Start by creating a new Markdown file named `single.md` in the desired location within your project.

2. **Add Metadata**: Open the `single.md` file and add the following metadata at the beginning:

   ```yaml
   ---
   layout: default
   title: Sample Single Page
   nav_order: 1
   ---
   ```

   - `layout`: This attribute determines the layout of the page. Common choices include `default` or `page`, depending on your project's needs.
   - `title`: Set the title of your page within the quotation marks.
   - `nav_order`: Specify the order of the page. Smaller numbers place the page higher in the navigation order.

   Ensure that there is a space after each colon (not a tab) in the metadata.

3. **Page Content**: Below the metadata, you can start adding the content of your single page. You can use standard Markdown syntax to format text, add images, and create links like this.
	```yaml
   ---
   layout: default
   title: Sample Single Page
   nav_order: 1
   ---
	**Put some important content here**
 
	```


   ![Single Page Image](/assets/images/github_page/adding-documentation/single_page.png)

4. **Metadata Importance**: It's crucial to include proper metadata in your Markdown files. Without it, Jekyll may not recognize the file, and your page won't be displayed on your website.

   {: .warning }
   Markdown files without proper metadata will not be shown by Jekyll.

By following these steps, you can create a single page with the necessary metadata to ensure proper organization and display within your Jekyll-based website.