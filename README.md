# thohi.github.io Guide

This repository contains the source code for a guide hosted at [thohi.github.io](https://thohi.github.io). The site is built using Jekyll.

## Prerequisites

Before you begin, ensure you have the following installed:
- Ruby
- RubyGems
- Bundler

You can check if you have Ruby and RubyGems installed by running:
`ruby -v`
`gem -v`

Install Bundler (if you haven't already):
`gem install bundler`

## Running Locally

1.  **Clone the repository (if you haven't already):**
    `git clone https://github.com/thohi/thohi.github.io.git`
    `cd thohi.github.io`

2.  **Install dependencies:**
    Navigate to the root directory of the project (where `Gemfile` is located) and run:
    `bundle install`

3.  **Serve the site:**
    `bundle exec jekyll serve --livereload`

    This will start a local development server. Open your web browser and go to `http://localhost:4000` (or the address shown in your terminal) to see the site. The `--livereload` flag automatically refreshes the page when you make changes to the source files.

## Adding Content

### Creating Posts

1.  Navigate to the `_posts` directory.
2.  Create a new file named in the format `YYYY-MM-DD-your-post-title.md`. For example, `2023-10-27-my-first-post.md`.
3.  Add YAML front matter and content to your post file. Example:

    ```markdown
    ---
    layout: post # Or another layout you define
    title: "My Awesome Post"
    date: YYYY-MM-DD HH:MM:SS +/-TTTT # Optional: if not present, uses date from filename
    categories: [category1, category2] # Optional
    tags: [tag1, tag2] # Optional
    ---

    Your post content goes here. You can use Markdown.
    ```

### Creating Pages

1.  Create a new Markdown (`.md`) or HTML (`.html`) file in the root directory or a subdirectory.
2.  Add YAML front matter. Example for a page in the root:

    ```markdown
    ---
    layout: default # Or another layout
    title: "My Custom Page"
    permalink: /my-custom-page/ # Optional: defines the URL
    ---

    Content for your page.
    ```

## Deployment

This site is configured to be deployed via GitHub Pages. Pushing changes to the `main` (or `master`) branch will automatically trigger a rebuild and deployment of the site.

## Theme

This site uses the [Minima](https://github.com/jekyll/minima) theme. You can customize it further by overriding its templates and styles. Refer to the Minima documentation for more details.
```
