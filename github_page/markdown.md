---
layout: default
title: "2. Markdown: The core of documenting"
nav_order: 2
parent: "Write Your Own Documentation!"
---

{: .warning}
Always **UPDATE** your own repo before doing any editing work!
- ![](/assets/images/github_page/adding-documentation/sync.png)

# All the documentation are markdown-based

Markdown is a lightweight markup language that allows you to format text on the web easily. It's widely used for creating documentation, README files, and forum posts. Markdown uses a simple and human-readable syntax to style your text. Here's a quick guide to get you started:

## Headers

To create headers, use the `#` symbol followed by a space. The number of `#` symbols determines the header level.

```
# Header 1
## Header 2
### Header 3
```

## Text Formatting

- **Bold**: Surround the text you want to make bold with `**` or `__`.

   ```
   **This is bold**
   __This is also bold__
   ```

- *Italic*: Use `*` or `_` around the text you want to italicize.

   ```
   *This is italic*
   _This is also italic_
   ```

- ~~Strikethrough~~: Enclose the text in `~~` to strike it through.

   ```
   ~~This is strikethrough~~
   ```

## Lists

### Ordered Lists

1. Item 1
2. Item 2
3. Item 3

To create an ordered list, use numbers followed by a period and a space.

### Unordered Lists

- Item A
- Item B
- Item C

To create an unordered list, use a `-`, `*`, or `+` followed by a space.

## Links

To create a link, use square brackets `[]` for the link text and parentheses `()` for the URL.

```
[OpenAI's website](https://www.openai.com)
```

## Images

Insert images using an exclamation mark `!`, square brackets `[]` for alt text, and parentheses `()` for the image URL.

```
![Alt text](https://www.example.com/image.jpg)
```

We recommend you use image hosting website like [imgur](https://imgur.com/upload) to store your image and insert your image with the above code.

## Quotes

To create blockquotes, use `>` before the text.

```
> This is a blockquote.
```

## Code

Inline code can be created using backticks \`code\`.

```
Use \`code\` for inline code.
```

For code blocks, enclose the code with triple backticks (```) and specify the programming language for syntax highlighting.

```python
def hello_world():
    print("Hello, world!")
```

## Horizontal Rule

To create a horizontal rule, use three or more hyphens (`---`), asterisks (`***`), or underscores (`___`) on a separate line.

```
---
```

## Escape Characters

If you want to display a character that has special meaning in Markdown (e.g., `*`, `[`, `]`), you can escape it using a backslash `\`.

```
\*This is not italic\*
```

## Callouts (Only applicable on this site)

Callouts are good for highlighting information added by the theme. Try the code below

```
{: .warning }
WARNING: This is a warning

{: .highlight }
This is a highlight

{: .note }
Note that this is a note

{: .new}
We just added a new callout
```

{: .warning }
WARNING: This is a warning

{: .highlight }
This is a highlight

{: .note }
Note that this is a note

{: .new}
We just added a new callout



