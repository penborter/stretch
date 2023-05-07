---
layout: post
tags: [Hello, Stretch]
photoloc: /assets/
toc: true
---

# Stretch Theme

Hello World! A quick run through of the key elements of this theme are below. 

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

Basically, the colours are swapped throughout when the button is clicked, with some minor exceptions that can be found in [layout.scss](https://github.com/penborter/stretch-theme/blob/main/_sass/layout.scss), under the `[data-theme="dark"]` styles. The two colour system will still work if the theme switch button isn't included. 

### List.html

You can choose how to display your collections using the [`list.html`](https://github.com/penborter/stretch-theme/blob/main/_layouts/list.html) layout. This layout has three versions, depending on the front matter you include in your page. See the template's [books](/books), [posts](/posts), and [projects](/projects) pages for examples of the three layouts.

1. A plain list of collection items - set `layout: list` with no other changes required. *E.g.: [Books](/books)*
2. A list of collection items separated by year - `layout: list` and `by_date: true` in the front matter. *E.g.: [Posts](/posts)*
3. A list of collection items as cards - set `layout: list` and `card: true` in the front matter. *E.g.: [Projects](/projects)*

For collections as cards, you can also set a thumbnail picture to use for each card. For that card's collection item, set `thumb` in the front matter to the desired url. Check out the sample gallery and `example.md` for an example.

### Page TOC

The Table of Contents at the bottom right is optional––just set `toc: true` in a page's front matter if you want to include it. It will display all headings H2 and below.

## Images

### Photo Layout

The `photo.html` layout allow you to make a horizontally-scrolling gallery of photos. An example can be found [here](https://stretch.ben.report/photos/example). The photos in the gallery are based on the `photo_id` url provided in the page's front matter, which is matched up with an equivalent entry in the site's `photos.yml` data file. The YAML entry for the set of photos should include all the relevant metadata, like photo file names, URLs, captions, titles, etc. 

Also included (via the `default.html` layout) is a small bit of JS that enables navigation through photos by arrow key presses. It can be found in the `_includes` folder, as `gallery_nav_js.html`. 

### Inline Images

The theme includes a `picture.html` file in the `_includes` folder for any photos you want to add to posts / pages. The usage is described [within the file](https://github.com/penborter/stretch/blob/main/_includes/picture.html). Images added this way can come in two sizes: normal (default), and wide which overflows the sidebar by default. Wide images' overflow amount is set by the `$pic-wide` variable in [`layout.scss`](https://github.com/penborter/stretch-theme/blob/main/_sass/layout.scss).

{% include picture.html
   file="stretching.png"
   class="wide"
%}

## Other Formatting

Below are a quick set of example components, to highlight the base theme formatting.

> If variety is sought in all the arts and amusements, such as archery and others, how much more should it be sought after in the art of love.

More complete blockquotes can also be made using the [`quote.html`](https://github.com/penborter/stretch-theme/blob/main/_includes/quote.html) includes element, which takes the author, title and even link to all be included and formatted within the blockquote.

{% include quote.html
content="We need more variety on the web. We need more people creating their own spaces on the web. Spaces that they own, spaces that they control. Spaces where they can share their creativity, personality, voice, experience, knowledge, skills. So if you feel that the web is getting boring, commodified and homogeneous, if you feel that the web is controlled by a handful of large corporations, this is one way that you can make a bit of a difference."

author="Marko Saric" title="How You Can Help Keep Blogging Alive"
link="https://markosaric.com/keep-blogging-alive/#more-28884"
%}

Inline code elements are shown throughout this post; below is a code block. Note that by default, code blocks do not change colour with the theme switch button. 

```python
# And here is a code block, using Python.

def doubleSize(fontSize):

   return fontSize * 2

h1FontSize = doubleSize(16)
```

H1 elements are used in this theme only for the initial page title, after which H2 and H3 elements are used. If you need more than three levels of headings, you're on your own. You might have noticed as well that H1 elements, by default, will not show up in the table of contents. 

# Header 1
## Header 2
### Header 3
