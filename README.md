# Stretch

A simple, flexible Jekyll theme for personal websites and blogs.

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

There are two key elements of the theme to highlight: the foreground and background colours, and the choice in how to display each collection.

### Two-colour system

Two colour variables can be used to set all the colours for the theme:

- `$fg` (foreground)
- `$bg` (background) 

Variations of these two colours are then derived and used throughout the site. It is recommended that you choose a pair of colours with a high contrast; at the very least you'll want to be able to read the `$fg`-coloured text on a `$bg`-coloured background.

### List.html

You can choose how to display your collections using the [`list.html`]() layout. This layout has three versions, depending on the front matter you include in your page. See the template's [books](), [posts](), and [projects]() pages for examples of the three layouts.

1. A plain list of collection items - set `layout: list` with no other changes required. *E.g.: [Books]()*
2. A list of collection items separated by year - `layout: list` and `by_date: true` in the front matter. *E.g.: [Posts]()*
3. A list of collection items as cards - set `layout: list` and `card: true` in the front matter. *E.g.: [Projects]()*

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/penborter/stretch. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Development

To set up your environment to develop this theme, run `bundle install`.

Your theme is setup just like a normal Jekyll site! To test your theme, run `bundle exec jekyll serve` and open your browser at `http://localhost:4000`. This starts a Jekyll server using your theme. Add pages, documents, data, etc. like normal to test your theme's contents. As you make modifications to your theme and to your content, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

When your theme is released, only the files in `_layouts`, `_includes`, `_sass` and `assets` tracked with Git will be bundled.
To add a custom directory to your theme-gem, please edit the regexp in `stretch.gemspec` accordingly.

## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

