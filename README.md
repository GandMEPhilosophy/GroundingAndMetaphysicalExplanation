---
layout: page
title: ""
---

## System set-up

1. Make a github account.
2. send it to Dika who will add you to the repo.

Download:
3. PyCharm (community edition)
4. Github desktop

5. Log into Github Desktop with your Github account. 
6. Go to the website repo on github.com and click on the large button that says 'clone'. 
7. Choose 'open with github desktop'. 
8. Choose where you want to save the repo locally. 
9. Press accept.

Once you see it in your GitHub desktop, click on 'open in Pycharm' in the middle of the screen. This
will open your repo in Pycharm and you'll be able to update/amend the code.

To see the local version of your website so you can see how your changes look, you'll need to host it locally. To do that:
10. Click on 'Terminal' at the bottom of your Pycharm screen.
11. If this is the first time youre doing this, you will need to type in 'bundle install' and enter. This will install the packages
you need to locally host. Skip this step if youve already done this.If this throws errors, contact Dika. You will only have to do this once.
12. Type 'bundle exec jekyll serve' to render the page locally. 
13. Click on the link you see in your terminal now (looks something like 127.0.0.0:localhost). This will open the local version
of the website in your browser. You can start applying changes now. Whenever you change something in the pycharm, refresh the page on your
browser to see how it looks.


## Updating the website

14. Before you start changing your code, go back to Github.com onto the repo and click on 'issues'.
15. Select the issue you want to work on or press 'new issue' and write in what you will do (e.g. 'update about page'). 
16. Press submit new issue. This will publish the issue to the repo so everyone knows the changes youre about to apply. 
17. On the right-hand side press on 'create branch'. Choose 'open branch with github desktop. 
18. Press the 'create branch' button. This will be the branch you will work on so your changes are not applied until they are finished.
19. Apply changes on your Pycharm (see instructions below). Check them using 'bundle exec jekyll serve'.
20. When youre happy with the changes, go to your GitHub desktop.
21. The changes youre about to push are on the left-hand side of the screen. Untick everything that starts with .idea/ or _site/ - those
are local files we dont need on the repo. Ensure the items which are ticked are only the ones you just worked on.
22. At the bottom of the left-hand side, type a summary of the changes (e.g. updated about page with contact details). 
23. Click on 'commit to [BRANCH NAME]'.
24. Press 'push origin' on the top line 

```ruby
gem "hitchens-theme"
```

And add the following lines to your Jekyll site's `_config.yml`:

```yaml
theme: hitchens-theme
```

Depending on your [site's configuration](https://jekyllrb.com/docs/configuration/options/), you may also need to add:

```yaml
ignore_theme_config: true
```

And then on the command line, execute:

    $ bundle

Or install the theme yourself as:

    $ gem install hitchens-theme

## Usage

### Home Layout

The `home` layout presents a list of articles ordered chronologically. The theme uses [Jekyll's built-in pagination](https://jekyllrb.com/docs/pagination/#enable-pagination) which can be configured in your `_config.yml` file.

The masthead of the home page is derived from the `title` and `description` set in your site's `_config.yml` file.

#### Navigation

To include a navigation menu in your site's masthead and footer:

1. Create a `_data` directory in the root of your site.
2. Add a `menu.yml` file to the `_data` directory.
3. Use the following format to list your menu items:

```
- title: About
  url: /about.html

- title: Source
  url: https://github.com/patdryburgh/hitchens
```

Be sure to start your `url`s with a `/`.

#### Pagination

To paginate your posts, add the following line to your site's `Gemfile`:

```
gem "jekyll-paginate"
```

Then, add the following lines to your site's `_config.yml` file:

```
plugins:
  - jekyll-paginate

paginate: 20
paginate_path: "/page/:num/"
```

You can set the `paginate` and `paginate_path` settings to whatever best suits you.

#### Excerpts

To show [excerpts](https://jekyllrb.com/docs/posts/#post-excerpts) of your blog posts on the home page, add the following settings to your site's `_config.yml` file:

```
show_excerpts: true
```

By default, excerpts that have more than 140 characters will be truncated to 20 words. In order to override the number of words you'd like to show for your excerpts, add the following setting to your site's `_config.yml` file:

```
excerpt_length: 20
```

To disable excerpt truncation entirely, simply set `excerpt_length` to `0` in your site's `_config.yml` file, like so:

```
excerpt_length: 0
```

If you do this, the theme will still respect Jekyll's `excerpt_separator` feature as [described in the Jekyll documentation](https://jekyllrb.com/docs/posts/#post-excerpts).


#### Title-less Posts

If you want to publish posts that don't have a title, add the following setting to the [front matter](https://jekyllrb.com/docs/frontmatter/) of the post:

```
title: ""
```

When you do this, the home page will display a truncated [excerpt](https://jekyllrb.com/docs/posts/#post-excerpts) of the first paragraph of your post.

Note that setting `excerpt_length` in your site's `_config.yml` file will set the length of _all_ excerpts, regardless of whether the post has a title or not. For posts with a title, the excerpt will appear under the title and slightly lighter. For title-less posts, the excerpt will appear as if it were a title.

### Post Layout

A sparsely decorated layout designed to present long-form writing in a manner that's pleasing to read.

To use the post layout, add the following to your post's [front matter](https://jekyllrb.com/docs/frontmatter/):

```
layout: post
```

### Icons

The [JSON Feed spec](https://jsonfeed.org/version/1) states that feeds should include an icon. To add your icon, add the following line in your site's `_config.yml` file:

```
feed_icon: /assets/images/icon-512.png
```

Then, replace the `/assets/images/icon-512.png` file with your own image.

### Credits

The theme credits that appear at the bottom of each page can be turned off by including the following line in your site's `_config.yml` file:

```
hide_credits: true
```

### Search

The theme uses a [custom DuckDuckGo Search Form](https://ddg.patdryburgh.com) that can be turned off by including the following line in your site's `_config.yml` file: 

```
hide_search: true
```

### Font

I spent a good amount of time trying to identify the font used on the front cover of the trade paperback version of Arguably. Unfortunately, I failed to accurately identify the exact font used. If you happen to know what font is used on the book cover, I would appreciate you [letting me know](mailto:hello@patdryburgh.com) :)

The theme includes a version of [EB Garamond](https://fonts.google.com/specimen/EB+Garamond), designed by Georg Duffner and Octavio Pardo. It's the closest alternative I could come up with that included an open license to include with the theme.

A [copy of the license](https://github.com/patdryburgh/hitchens/blob/master/assets/fonts/OFL.txt) has been included in the `assets` folder and must be included with any distributions of this theme that include the EB Garamond font files.

## Contributing & Requesting Features

Bug reports, feature requests, and pull requests are welcome on GitHub at [https://github.com/patdryburgh/hitchens](https://github.com/patdryburgh/hitchens).

This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Development

To set up your environment to develop this theme, run `bundle install`.

The theme is setup just like a normal Jekyll site. To test the theme, run `bundle exec jekyll serve` and open your browser at `http://localhost:4000`. This starts a Jekyll server using the theme. Add pages, documents, data, etc. like normal to test the theme's contents. As you make modifications to the theme and to your content, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

## License

The code for this theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

The font, EB Garamond, is Copyright 2017 The EB Garamond Project Authors and licensed under the [SIL Open Font License Version 1.1](https://github.com/patdryburgh/hitchens/blob/master/assets/fonts/OFL.txt).

Graphics are released to the public domain.
