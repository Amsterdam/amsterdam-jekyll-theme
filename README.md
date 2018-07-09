# City of Amsterdam Jekyll theme

A jekyll theme for the set up of quick generic static sites and for use with GitHub pages and/or Jekyll in the [webdesign of the City of Amsterdam](https://patternlab-amsterdam.infoprojects.nl/).

## Building locally

This theme is built to run predictably on GitHub pages, therefore the [`github-pages`](https://github.com/github/pages-gem) gem is required. Run `bundle install` before building with Jekyll.

To serve locally with Jekyll, use `bundle exec jekyll serve`.

## Configuring and customising

The configuration of this theme can be done mostly in [Jekyll's `_config.yml`](https://jekyllrb.com/docs/configuration/). To replace sections of the site you can overwrite [the `_includes`](https://jekyllrb.com/docs/includes/) and add [new `_layouts`](https://jekyllrb.com/docs/themes/#overriding-theme-defaults).

### Header

You can replace the header by putting a `header.liquid` file in the folder `_includes`.

#### The Amsterdam Open Source logo

You can hide the logo in the top by adding the following to your `_config.yml`.

```yaml
headerHideLogo: true
```

You can change the logo by adding a file named `logo.svg` in the folder `assets`.

#### The site title

You can hide the site title in the top by adding the following to your `_config.yml`.

```yaml
headerHideTitle: true
```

### Top navigation

To place your own links in the top navigation create a file called `top-nav.liquid` in the folder `_includes`. The top navigation expects an `ul` populated by `li`s with links in them.

For example:

```html
<ul>
  <li>
    <a href="{{ site.baseurl }}/">Home</a>
  </li>
  <li>
    <a href="{{ site.baseurl }}/projects/">Projects</a>
  </li>
  <li>
    <a href="{{ site.baseurl }}/guides/">Guides</a>
  </li>
</ul>
```

### Footer

To place your own content in the footer create a file called `footer.liquid` in the folder `_includes`. The footer expects up to 4 `article` tags as columns. These can feature `h3`s as headers, `ul`/`li` lists of links or any other content.

## Licence

© The City of Amsterdam 2018. Licenced MPL 2.0, see the [`LICENSE`](LICENSE) file for more information.
