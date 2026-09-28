# Chirpy Starter

[![Gem Version](https://img.shields.io/gem/v/jekyll-theme-chirpy)][gem]&nbsp;
[![GitHub license](https://img.shields.io/github/license/cotes2020/chirpy-starter.svg?color=blue)][mit]

A minimal, ready-to-use template for creating a blog with the [**Chirpy**][chirpy] Jekyll theme. Get up and running in minutes with all critical files pre-configured.

## Why This Starter Exists

When installing Chirpy through [RubyGems.org][gem], Jekyll can only read a subset of theme files (`_data`, `_layouts`, `_includes`, `_sass`, `assets`) and limited `_config.yml` options from the gem. As a result, users cannot enjoy the full out-of-the-box experience that Chirpy offers.

To unlock all features, the following files must be present in your Jekyll site:

```shell
.
├── _config.yml
├── _plugins
├── _tabs
└── index.html
```

This starter bundles those files from the latest **Chirpy** release along with a [CD][CD] workflow, so you can start writing immediately.

## Usage

Check out the [theme's docs](https://github.com/cotes2020/jekyll-theme-chirpy/wiki).

## Decap CMS

The CMS is available at <https://vanillaturtlechips.github.io/admin/>.
It edits posts in `_posts/` and stores uploaded images in `assets/img/uploads/`.

The GitHub backend requires an OAuth server before the first login. GitHub
Pages only hosts the CMS UI, so choose one of these authentication options:

- **Decap Turbo:** sign up at <https://turbo.decapcms.org/signup>, create a site
  for this repository, then replace the `backend` block in
  `admin/config.yml` with the `turbo-github` configuration and the generated
  `turbo_site_id`.
- **Self-hosted OAuth proxy:** create a GitHub OAuth App and deploy an OAuth
  proxy such as the [Decap Cloudflare Worker template][decap-proxy]. Set its
  URL as `backend.base_url` and its auth path as `backend.auth_endpoint`.

After authentication is configured, open `/admin/` and sign in with an account
that has write access to this repository.

The CMS creates editorial workflow pull requests. Merging one updates the
Markdown source, which triggers the existing GitHub Pages workflow.

[decap-proxy]: https://github.com/sterlingwes/decap-proxy

## Contributing

This repository is automatically updated with new releases from the theme repository. If you encounter any issues or want to contribute to its improvement, please visit the [theme repository][chirpy] to provide feedback.

## License

This work is published under [MIT][mit] License.

[gem]: https://rubygems.org/gems/jekyll-theme-chirpy
[chirpy]: https://github.com/cotes2020/jekyll-theme-chirpy/
[CD]: https://en.wikipedia.org/wiki/Continuous_deployment
[mit]: https://github.com/cotes2020/chirpy-starter/blob/master/LICENSE
