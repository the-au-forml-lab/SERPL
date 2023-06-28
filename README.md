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

### Notes on upgrading

The page templates are set in the _config.yml. To add a newer event:

1. make a new layout in _layouts (see. e.g. 2023.html in layout)
2. change the config to use that new layout (see `defaults` in config.yml)

The "old" events will retain their layout using the scoped paths.