---
layout: default
title: "Add a Collection"
nav_order: 4
parent: "3. Organize your Pages"
grand_parent: Write Your Own Documentation!
---

{: .warning}
Always **UPDATE** your own repo before doing any editing work!
- ![](/assets/images/github_page/adding-documentation/sync.png)

# How to add a Collection
1. Create a folder called `_things`, remember you must put an **underscore** `_` before the name 

2. Edit the `_config.yml` to add the following lines under the `collections` field, the collection name must match the folder name except the underscore

	```yml
	collections:
	  # ... omitting previous collections ...
	  things:
	    permalink: ":/collection/:path/"
	    output: true
	```

3. And find the line `just_the_docs`, add the collection you just defined

	```yml
	just_the_docs:
	  collections:
	  # ... omitting previosus collections ...
	    things:
	      name: "Things"
	```
	
4. And create a single page or page with child in the folder, here I just moved the `animals` folder we created in the last article inside the `_things`

Here we go

![](/assets/images/github_page/adding-documentation/collection.png)

Some notes:
1. You can change the order of the collection by rearranging the order inside the `just_the_docs` -> `collections`.
2. Remember to match the names defined in `collections` and `just_the_docs` -> `collections`.
3. After you add a collection, run `bundle exec jekyll serve` again to see the effects.


