# SERPL Website

Website for The Southeast Regional Programming Languages Seminar (SERPL).

## Development Notes

This website is built with markdown, [Jekyll](https://jekyllrb.com/), [Bootstrap](https://getbootstrap.com/docs/5.2/getting-started/introduction/) and hosted by [Github Pages](https://pages.github.com/).

For small changes it is sufficient to make changes to the markdown and then commit and push those changes.
The website will update automatically.

### Debugging the website locally

1. Setup environment: 
   - To install Jekyll for various OS: <https://jekyllrb.com/docs/installation>
   - You will need at least Ruby, and
   - Ruby gems bundler and jekyll: `gem install jekyll bundler`
   - Also needed [this](https://github.com/jekyll/jekyll/issues/8523): `bundle add webrick`
   
2. See instructions of how to [debug pages locally](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll#building-your-site-locally).
   Generally, once the dependencies are set up, run:
   
    ```
    bundle exec jekyll serve
    ```

### Notes on templating

All page templates are configured in `_config.yml`. To add a new event:

1. make a new layout in `_layouts/` (see `2023.html` as example)
2. apply that new layout to selected scope (see `defaults` in `_config.yml`)

Existing events will retain their layout using the scoped paths.