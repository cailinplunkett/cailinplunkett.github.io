# Cailin Plunkett

## Updating Header and Footer Links

Links in the header and footer are auto-generated. Links will be made for all files marked `category: page`, that have a title, and have the custom `main_nav` front-matter variable set to `true`. You can modify the rules for link generation in `_layouts/nav_links.html`.

## Updating Styles

If you want change the CSS of the theme, you'll probably want to check out these files in the `_sass/` directory:

* `base/_variables.scss`: Common values found throughout the project, including base font size, font families, colors, and more.
* `base/_typography.scss`: Base typography values for the site (see `typography.html` for a demonstration)
* `_layout.scss`: The primary styles for the layout and design of the theme.

### Important Variables

Here are the important variables from `base/_variables.scss` you can tweak to customize the theme to your liking:

* `$base-font-family`: The font-family of the body text. Make sure to `@import` any new fonts!
* `$heading-font-family`: The font-family of the headers. Make sure to `@import` any new fonts!
* `$base-font-size`: The base font-size. Defaults to $em-base from Bourbon (`bourbon/settings/_px-to-em.scss`).
* `$base-font-color`: The color for the body text.
* `$action-color`: The color for links in the body text.
* `$highlight-color`: The color for the footer and page headers (when no cover image provided).

## Configuration

All configuration options can be found in `_config.yml`.

### Site Settings

* __title:__ The title for your site. Displayed in the navigation menu, the `index.html` header, and the footer.
* __subtitle:__ The subtitle of your site. Displayed in the `index.html` header.
* __email:__ Your email address, displayed with the Contact info in the footer.
* __name:__ Your name. _Currently unused._
* __description:__ The description of your site. Used for search engine results and displayed in the footer.
* __baseurl:__ The subpath of your site (e.g. /blog/).
* __url:__ The base hostname and protocol for your site.
* __cover:__ The relative path to your site's cover image.
* __logo:__ The relative path to your site's logo. Used in the navigation menu instead of the title if provided.

### Build Settings

* __markdown:__ Markdown parsing engine. Default is kramdown.
* __inter_post_navigation:__ Whether to render links to the next and previous post on each post.

### Pagination settings

See the documentation for [jekyll-paginate-v2](https://github.com/sverrirs/jekyll-paginate-v2/blob/master/README-GENERATOR.md#site-configuration) for more details.

### Archive Settings

Although this theme comes with a combined, categorized archive (see `posts.html`), you can enable further archive creation thanks to [jekyll-archives][archives]. Support for category and tag archive pages is included, but you can also add your own archive pages for years, months, and days.

To change archive settings, see the __jekyll-archives__ section of `_config.yml`:

```yml
jekyll-archives:
  enabled:
    - categories
    - tags
  layout: 'archive'
  permalinks:
    category: '/category/:name/'
    tag: '/tag/:name/'
```

To fully disable the archive, remove the __jekyll-archives__ section AND remove it from the __gems__ list.

__NOTE:__ the Jekyll Archive gem is NOT included with GitHub pages! Disable the archive feature if you intend to deploy your site to GitHub pages. [Here is a guide](http://ixti.net/software/2013/01/28/using-jekyll-plugins-on-github-pages.html) on how you can use the `jekyll archive` gem with GitHub pages. The general gist: compile the Jekyll site locally and then push that compiled site to GitHub.

A sitemap is also generated using [jekyll-sitemap][sitemap].

### Syntax Highlighting Settings

Inside of a post, you can enable syntax highlighting with the `{% highlight <language> %}` Liquid tag. For example:

```
{% highlight javascript %}
function demo(string, times) {
  for (var i = 0; i < times; i++) {
    console.log(string);
  }
}
demo("hello, world!", 10);
{% endhighlight %}
```

You can change the [HighlightJS theme][highlightjs_theme] in `_config.yml`:

```yml
highlightjs_theme: "monokai_sublime"
```

### Disqus Settings

You can enable [Disqus][disqus] comments for you site by including one config option:

* __disqus_shortname:__ Your Disqus username. If the property is set, Disqus comments will be included with your blog posts.

If you want to disable Disqus for only a specific page, add __disqus_disabled: true__ to the page's front matter.

### Google Analytics Settings

You can enable basic [Google Analytics][ga] pageview tracking by including your site's tracking ID:

* __ga_tracking_id__: The Tracking ID for your website. You can find it on your Google Analytics dashboard. If the property is set, Google Analytics will be added to the footer of each page.

### Social Settings

Your personal social network settings are combined with the social sharing options. In the __social__ section of `_config.yml`, include an entry for each network you want to include. For example:

```yml
social:
  - name: Twitter                         # Name of the service
    icon: twitter                         # Font Awesome icon to use (minus fa- prefix)
    username: TheBenCentra                # (User) Name to display in the footer link
    url: https://twitter.com/TheBenCentra # URL of your profile (leave blank to not display in footer)
    desc: Follow me on Twitter            # Description to display as link title, etc
    share: true                           # Include in the "Share" section of posts
```


### Category Descriptions

You can enhance the `posts.html` archive page with descriptions of your post categories. See the __descriptions__ section of `_config.yml`:

```yml
# Category descriptions (for archive pages)
descriptions:
  - cat: jekyll
    desc: "Posts describing Jekyll setup techniques."
```


## License

MIT. See [LICENSE.MD](https://github.com/bencentra/centrarium/blob/master/LICENSE.md).

[bencentra]: http://bencentra.com
[bourbon]: http://bourbon.io/
[neat]: http://neat.bourbon.io/
[bitters]: http://bitters.bourbon.io/
[refills]: http://refills.bourbon.io/
[fontawesome]: http://fortawesome.github.io/Font-Awesome/
[highlightjs]: https://highlightjs.org/
[highlightjs_theme]: https://highlightjs.org/static/demo/
[lightbox]: http://lokeshdhakar.com/projects/lightbox2/
[cover]: https://www.flickr.com/photos/79666107@N00/3796678503/in/photolist-6MuYfc-61Rtft-8XzPmY-a6Cozm-54eSMs-6oMJmk-aepZQq-9YkPHp-fiAEGE-dVP4Z5-oxPyJP-atKUFJ-9YHWA5-9YF2f2-9YF2gR-9YHVGN-9YHVvs-qZYYQ6-4JqP2i-a2peGy-9YHVUm-9YHVF7-9YHVCL-9YF3NK-cYteMo-aiPmb9-69dtAi-9YF21x-4aWpmn-7SLiUL-77pqVX-8vXbYv-4HGDSH-a2h5P1-8LsZrQ-9aj1ez-auPZ7q-9YHVMd-9YF2bi-9YF23D-8LpWpn-9an6KL-9YHVZL-dqZ3Cz-2GuvnX-9YHWUo-9YHVWd-p5Roh5-i1zTbv-6sYrUT
[disqus]: https://disqus.com/
[ga]: http://www.google.com/analytics/
[archives]: https://github.com/jekyll/jekyll-archives
[sitemap]: https://github.com/jekyll/jekyll-sitemap
