---
layout: post
tags: [Hello, Stretch]
photoloc: /assets/
toc: true
---

# Stretch Theme

Hello World! 

## Table of Contents

The Table of Contents to the right is optional–just set `toc: true` if you want to include it.

## Usage

There are two key elements of the theme to highlight: the foreground and background colours, and the choice in how to display each collection.

### Two-colour system

Two colour variables can be used to set all the colours for the theme:

- `$dark`
- `$light`

Variations of these two colours are then derived and used throughout the site. It is recommended that you choose a pair of colours with a high contrast; at the very least you'll want to be able to read the `$dark`-coloured text on a `$light`-coloured background. 

[Here](https://randoma11y.com/) is a suggested resource for generating two-colour pairs.

### Theme Switch / Dark-Light mode

The theme includes a JS-based theme switch button based on the two theme colours `$dark` and `$light`. 

Basically the colours are swapped throughout when the button is clicked, with some minor exceptions that can be found in [layout.scss](https://github.com/penborter/stretch-theme/blob/main/_sass/layout.scss), under the `[data-theme="dark"]` styles. The two colour system will still work if the theme switch button isn't included. 

### List.html

You can choose how to display your collections using the [`list.html`](https://github.com/penborter/stretch-theme/blob/main/_layouts/list.html) layout. This layout has three versions, depending on the front matter you include in your page. See the template's [books](/books), [posts](/posts), and [projects](/projects) pages for examples of the three layouts.

1. A plain list of collection items - set `layout: list` with no other changes required. *E.g.: [Books](/books)*
2. A list of collection items separated by year - `layout: list` and `by_date: true` in the front matter. *E.g.: [Posts](/posts)*
3. A list of collection items as cards - set `layout: list` and `card: true` in the front matter. *E.g.: [Projects](/projects)*

## Images

The theme includes a `picture.html` file in the `_includes` folder for any photos you want to add. The usage is described in the [includes file on Github](https://github.com/penborter/stretch/blob/main/_includes/picture.html). 

{% include picture.html
   file="stretching.png"
%}

## Other Formatting

Other formatting examples are below.

> Here is a blockquote.

Inline code blocks are shown above, and below is a code block. 

```python
# And here is a code block, using Python.

def doubleSize(fontSize):

   return fontSize * 2

h1FontSize = doubleSize(16)
```

# Header 1
## Header 2
### Header 3
More than three levels of headings is too many––go back up to level 3. 