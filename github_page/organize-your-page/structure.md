---
layout: default
title: "Folder structure"
nav_order: 1
parent: "2. Organize your Pages"
grand_parent: Write Your Own Documentation!
---


# The Structure
```
.
├── assets
│   └── images
├── _coding
│   └── landmarks
│       └── index.md
├── github_page
│   ├── fork.md
│   ├── index.md
│   ├── markdown.md
│   ├── organize-your-page.md
│   ├── review-submission.md
│   └── setup-github-pages.md
└── _server_management
    └── user_management
        ├── adding-ssh-key.md
        └── index.md
```
(Some folders and files are omitted)

## Default Folders

These folders are either created or used by Jekyll by default to help structure your project:

### `assets`
This folder contains static assets such as images, stylesheets, or scripts. It's where you store all the visual and functional elements of your project.

## Custom Folders

These folders are created by us to help organize the project-specific documentation, you can always add more folders later:

### `github_page`
The `github_page` folder houses the documentation for the "*Writing Your Own Documentation*" page and contains all its child pages. This structure is particularly useful for maintaining a hierarchy of related content.

### `_coding`
The `_coding` folder serves as a **collection** named "Coding." Inside the `_coding` collection, there's an additional folder named `landmarks` to further organize content. This nesting allows for even finer categorization of documentation.

### `_server_management`
The `_server_management` folder acts as another **collection** named "Server Management." Collections are ideal for categorizing pages related to a particular theme or subject.

{: .note}
> Pages with children vs. Collection Collections:
> - Pages with children are pages that have a set of child pages. These parent pages can have their own content and can be organized within collections if necessary.
> - Collections, like "Coding" and "Server Management," are sets of pages grouped together for a specific purpose. Collections cannot be nested within other collections, and their folder names must start with an underscore `_`.