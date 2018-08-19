Source code for [https://dvnguyen.com](https://dvnguyen.com)

# Intro
The content is written in Markdown, and generated by an in-house, simple site generator in Python.

# Directory Structure
`content`: Contains content written in Markdown. You write your site's content here.

`output`: Contains generated html files. Static assets are also copied here after `build` command.

`template`: Contains Jinja2 template files. You can modify the templates here.

`static`: Contains static assets, including js, css, and images.

# Usage
## Write content
To write your site's content, add and edit the markdown files in the `content` directory.

### `content` directory structure
The structure of `content` directory assembles your site's structure. For instance, if following is your site's structure:

```
example.com
example.com/about.html
example.com/contact.html
example.com/posts/post1.html
example.com/posts/post2.html
```

,then the `content` directory will be:

```
content/_index.md
content/about.md
content/contact.md
content/posts/_index.md
content/posts/post1.md
content/posts/post2.md
```

Markdown files named `_index.md` is our convention for the index page of a directory.

### Headers in Markdown files
The header section of each Markdown file allows you to specify the template file. Template files can be found and editted in the `template` directory.

# Technical Decisions
This section lists our technical decisions for the site generator.

The project use `jinja2` for html template, and `mistletoe` for rendering Markdown content.