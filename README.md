# Sandeep Ghosh Portfolio Site

This repository contains the source code for my personal portfolio website, built with [Hugo](https://gohugo.io/) and the [Congo](https://jpanther.github.io/congo/) theme. The site is designed to be fast, simple to maintain, and easy to deploy on Cloudflare Pages.

The portfolio highlights my background as a software developer, with a focus on reliable systems, cloud technologies, Pega, Kubernetes, and production-ready engineering work. It currently includes a profile-style homepage and a custom contact page.

## Tech Stack

- Hugo extended
- Congo theme
- TOML-based Hugo configuration
- Custom CSS for page-level styling
- Formspree for contact form submissions
- Cloudflare Pages for deployment

## Project Structure

```text
.
├── assets/                 # Hugo-managed assets such as images
├── config/_default/        # Main Hugo configuration
├── content/                # Site pages and markdown content
├── layouts/                # Theme overrides and custom templates
├── static/                 # Static files such as CSS
├── _vendor/                # Vendored Hugo modules/themes
├── go.mod / go.sum         # Hugo module dependencies
└── .gitignore
```

## Current Site Content

- Home page with profile layout and author summary
- Contact page with a custom styled form
- Author metadata and social links configured through Hugo
- Theme override support for custom behavior when needed

## Local Development

### Requirements

- Hugo extended installed locally
- Go installed if you plan to work with Hugo modules

### Run Locally

```bash
hugo server
```

If port `1313` is already in use, run:

```bash
hugo server --port 1314
```

Then open the local server URL shown by Hugo in your browser.

## Build

To generate the production site:

```bash
hugo
```

The generated site output is written to the `public/` directory, which is ignored in Git.

## Configuration Notes

The primary Hugo configuration for this project lives under `config/_default/`. The root-level `config.toml` may still exist for compatibility or earlier setup, but the active site configuration is organized in the `config/` directory.

Key settings include:

- `config/_default/hugo.toml` for base site configuration
- `config/_default/params.toml` for theme and homepage settings
- `config/_default/languages.en.toml` for author details and language-specific metadata

## Contact Form

The contact page uses Formspree to handle form submissions. If you fork this project or reuse the contact page, update the form `action` URL in `content/contact.md` to point to your own Formspree endpoint.

## Deployment

This site is intended to be deployed on Cloudflare Pages.

Typical Cloudflare Pages settings:

- Build command: `hugo`
- Build output directory: `public`

Depending on your Cloudflare setup, you may also need to ensure the Hugo version is compatible with the theme and module setup used in this repository.

## Why This Repo Is Public

This repository is public to document how the site is structured, track changes over time, and make it easier to maintain or extend in the future. It also serves as a small reference project for a Hugo-based personal site with theme overrides and a custom contact page.

## License

This repository includes a `LICENSE` file. Please review it before reusing code or content from this project.
