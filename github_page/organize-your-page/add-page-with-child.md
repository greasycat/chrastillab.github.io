---
layout: default
title: "Add a Page with Child Pages"
nav_order: 3
parent: "3. Organize your Pages"
grand_parent: Write Your Own Documentation!
---


# How to Add a new Page with child pages
Let's be more organized by create pages with child pages. For example we want to write some docs on animals

1. Create a folder called `animals` or `ANIMALS` or `AniMals` (folder name is arbitrary but better keep them in lowercases)

2. Create an `index.md` to tell reader what the animals is 
	
	```
	---
	layout: default
	title: "Cute Animals"
	nav_order: 0
	has_children: true
	---
	```
	
	- `has_children: true`: this new attributes is what makes the parent page different from a single page
	
3. Create an `felis-catus.md` 

	```
	layout: default
	title: Felis Catus
	nav_order: 1
	parent: "Cute Animals"
	```
	
	- `parent: Animals`: you must specify the parent page's **title** (not folder name) 
	
Here's our new animal page
- ![](/assets/images/github_page/adding-documentation/page_with_child.png)

# Adding a Grandchild Page

In your Jekyll theme, you can create a grandchild page by following these steps. Please note that this example assumes that your theme supports a maximum of three levels of nesting for pages:

1. **Create a Folder for the Child**: Start by creating a folder for the child page. This folder will contain both the child and grandchild pages. Give this folder a descriptive name related to your content.

   ```plaintext
   ├── _pages/
   │   ├── parent/
   │   │   ├── index.md          # Parent page
   │   │   ├── child/
   │   │   │   ├── index.md      # Child page
   │   │   │   ├── grandchild/
   │   │   │   │   ├── index.md  # Grandchild page
   ```

2. **Create the Child Page**: Inside the child folder, create an `index.md` file for the child page. This is where you will add the content for the child page.

   ```markdown
   ---
   layout: default
   title: Child Page
   parent: Parent Page
   grand_parent: Grandparent Page
   nav_order: 2
   ---
   
   # Child Page

   This is the content of the child page.
   ```

   - `layout`: Set the layout for the child page (e.g., `default`).
   - `title`: Specify the title of the child page.
   - `parent`: Link the child page to its parent page (Replace "Parent Page" with the actual parent's title).
   - `grand_parent`: Link the child page to its grandparent page (Replace "Grandparent Page" with the actual grandparent's title).
   - `nav_order`: Determine the order in the navigation (if applicable).

3. **Create the Grandchild Page**: Inside the `grandchild` folder (inside the child folder), create an `index.md` file for the grandchild page. This is where you will add the content for the grandchild page.

   ```markdown
   ---
   layout: default
   title: Grandchild Page
   parent: Child Page
   grand_parent: Grandparent Page
   nav_order: 1
   ---
   
   # Grandchild Page

   This is the content of the grandchild page.
   ```

   - `layout`: Set the layout for the grandchild page (e.g., `default`).
   - `title`: Specify the title of the grandchild page.
   - `parent`: Link the grandchild page to its parent page (in this case, "Child Page").
   - `grand_parent`: Link the grandchild page to its grandparent page (in this case, "Grandparent Page").
   - `nav_order`: Determine the order in the navigation (if applicable).

4. **Navigation and Hierarchy**: Depending on your theme and configuration, the navigation and hierarchy of your pages may be automatically generated based on the metadata you provided. Make sure to adjust the `nav_order` values to control the order in which these pages appear in the navigation menu.

By following these steps, you can create a grandchild page with proper metadata and hierarchy in your Jekyll theme, allowing for up to three levels of nesting.

