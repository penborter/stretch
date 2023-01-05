# Stretch

A simple, flexible Jekyll theme for personal websites and blogs. Currently the theme contains no Javascript.

See a live example [here](http://stretch.penborter.com).

## Installation

Add this line to your Jekyll site's `Gemfile`:

```ruby
gem "stretch"
```

And add this line to your Jekyll site's `_config.yml`:

```yaml
theme: stretch
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install stretch

## Usage

### Two-colour system

Two colour variables can be used to set all the colours for the theme:

- `$fg` (foreground)
- `$bg` (background) 

Variations of these two colours are then derived and used throughout the site. It is recommended that you choose a pair of colours with a high contrast; at the very least you'll want to be able to read the `$fg`-coloured text on a `$bg`-coloured background.

### List.html

You can choose how to display your collections using the [`list.html`]() layout. This layout has three versions, depending on the front matter you include in your page. See the template's [books](http://stretch.penborter.com/books), [posts](http://stretch.penborter.com/posts), and [projects](http://stretch.penborter.com/projects) pages for examples of the three layouts.

1. A plain list of collection items - set `layout: list` with no other changes required. *E.g.: [Books](http://stretch.penborter.com/books)*
2. A list of collection items separated by year - `layout: list` and `by_date: true` in the front matter. *E.g.: [Posts](http://stretch.penborter.com/posts)*
3. A list of collection items as cards - set `layout: list` and `card: true` in the front matter. *E.g.: [Projects](http://stretch.penborter.com/projects)*

### Other Notes

- An atom / RSS feed (through the jekyll-feed ) is available at `/feed.xml`.
- 

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/penborter/stretch. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

