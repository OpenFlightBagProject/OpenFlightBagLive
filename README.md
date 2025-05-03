# OpenFlightBag Documentation Site

This directory contains the documentation site for the OpenFlightBag project. The site is deployed to GitHub Pages and serves both static documentation and the Flutter web application.

## Directory Structure

- `/docs/site/` - Root directory for documentation content
  - `/docs/site/app/` - Placeholder directory for the Flutter web app (populated during build)
  - `/docs/site/index.html` - Main landing page

## How It Works

1. The documentation content in this directory is committed to the repository
2. The Flutter web app is built during CI and placed in the `/docs/site/app/` directory
3. The combined content is published to GitHub Pages

## Adding Documentation

To add more documentation to this site:

1. Create new HTML or Markdown files in this directory
2. Reference them from the index.html file
3. Commit the changes to the repository

## Local Development

To preview the site locally:

1. Build the Flutter web app: `cd openflightbag_app && flutter build web --release --base-href /app/`
2. Copy the build output to the app directory: `cp -r openflightbag_app/build/web docs/site/app/`
3. Serve the site using a local web server: `cd docs/site && python -m http.server 8000`
4. Open http://localhost:8000 in your browser

## Notes

- The `/docs/site/app/` directory is ignored by Git (listed in .gitignore)
- Only add documentation content to this directory, not build artifacts