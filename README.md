# Git version control on both repo

```shell
git add -u
git commit -m "Update site"
git push origin main
git push sub main
```

# Check workflow

# Action plan

## Step 1

Fill in info `_config.yml`

## Step 2 — Add avatar 

Copy my photo to `assets/img/avatar.jpg`. Any square JPG/PNG works. 

## Step 3 — Fill in my homepage

Edit `index.html` 

## Step 4 — Fill in the other pages (20 min)

Edit `_tabs/about.md`, `_tabs/research.md`, `_tabs/projects.md`, `_tabs/cv.md` — same pattern: replace placeholders.

## Step 5 — Local preview (5 min)

`bundle install`
`bundle exec jekyll serve --livereload`
`# → open http://127.0.0.1:4000`
Or use the VSCode task: `Ctrl+Shift+P` → `Tasks: Run Build Task`.

## Step 6 — Deploy

Push to `main`. GitHub Actions will build and deploy automatically. Check the Actions tab for status.

# Common beginner mistakes to avoid

- Don't change `baseurl` — it's empty on purpose for `username.github.io` repos
- Don't rename `index.html` to `index.md` — Jekyll treats them differently
- Tab order is controlled by `order`: in front matter, not by filename
- The sidebar nav comes from `_tabs/` — add/remove pages by adding/removing files there
- Blog posts go in `_posts/` with filename format `YYYY-MM-DD-title.md`
- Avatar must start with `/` in the config path (`/assets/img/avatar.jpg`), not a relative path

# Chirpy Starter

[![Gem Version](https://img.shields.io/gem/v/jekyll-theme-chirpy)][gem]&nbsp;
[![GitHub license](https://img.shields.io/github/license/cotes2020/chirpy-starter.svg?color=blue)][mit]

When installing the [**Chirpy**][chirpy] theme through [RubyGems.org][gem], Jekyll can only read files in the folders
`_data`, `_layouts`, `_includes`, `_sass` and `assets`, as well as a small part of options of the `_config.yml` file
from the theme's gem. If you have ever installed this theme gem, you can use the command
`bundle info --path jekyll-theme-chirpy` to locate these files.

The Jekyll team claims that this is to leave the ball in the user’s court, but this also results in users not being
able to enjoy the out-of-the-box experience when using feature-rich themes.

To fully use all the features of **Chirpy**, you need to copy the other critical files from the theme's gem to your
Jekyll site. The following is a list of targets:

```shell
.
├── _config.yml
├── _plugins
├── _tabs
└── index.html
```

To save you time, and also in case you lose some files while copying, we extract those files/configurations of the
latest version of the **Chirpy** theme and the [CD][CD] workflow to here, so that you can start writing in minutes.

## Usage

Check out the [theme's docs](https://github.com/cotes2020/jekyll-theme-chirpy/wiki).

## Contributing

This repository is automatically updated with new releases from the theme repository. If you encounter any issues or want to contribute to its improvement, please visit the [theme repository][chirpy] to provide feedback.

## License

This work is published under [MIT][mit] License.

[gem]: https://rubygems.org/gems/jekyll-theme-chirpy
[chirpy]: https://github.com/cotes2020/jekyll-theme-chirpy/
[CD]: https://en.wikipedia.org/wiki/Continuous_deployment
[mit]: https://github.com/cotes2020/chirpy-starter/blob/master/LICENSE


