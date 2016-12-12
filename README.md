# jekyll-theme-cedar

A theme for blogs, for Jekyll and Siteleaf.

## Installation

Add the theme's gem to your site's `Gemfile`:

```ruby
gem "jekyll-theme-cedar"
```

Specify the `theme` in your site's `_config.yml`:

```yaml
theme: jekyll-theme-cedar
```

Install:

```
$ bundle
```

## Usage

### Configuration

You can set the following options in your site's `_config.yml`:

Setting | Description | Default
--- | --- | ---
`per_page` | Number of posts to display in the home index page | 10
`show_date` | Boolean to show date | `true`
`date_format` | Date [format](https://shopify.github.io/liquid/filters/date/) | `"%b %-d, %Y"` (outputs to `Jun 7, 2016`)
`footer_text` | (Markdown) text to include in the footer; footer will be hidden if not included |

### Custom styles

The theme comes with a stylesheet, `/assets/styles.scss`, where you can edit variables, including font sizes and colors.

### Additional pages

You can create additional pages, like an About page (`about.markdown`), which will be compiled at the URL `/about/`. Pages inherit the `post.html` layout by default.

```
---
title: About
---

This is the body of the page.
```

### Navigation

You can show navigation page links (both internal and external) in a horizontal list below the title. Add these in `_config.yml`:

```yaml
nav:
- title: About
  url: /about/
- title: GitHub
  url: https://github.com/justinjaywang/jekyll-theme-cedar
```

### Google Analytics

You can enable Google Anaytics in production in your site's `_config.yml` by specifying the tracking code:

```yaml
google_analytics: UA-XXXXXXXX-X
```

## Development

To set up your environment to develop this theme, run `bundle install`.

You theme is setup just like a normal Jekyll site. To test your theme, run `bundle exec jekyll serve` and open your browser at `http://localhost:4000`. This starts a Jekyll server using your theme. Add pages, documents, data, etc. like normal to test your theme's contents. As you make modifications to your theme and to your content, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

When your theme is released, only the files in `_layouts`, `_includes`, and `_sass` tracked with Git will be released.

## License

The theme is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

