# shagen.me

Personal website for Stefan Hagen, built with Astro and deployed to GitHub Pages.

## Features

- Minimal particle animation landing page
- Blog with Markdown support
- Static page generation
- Automated deployment via GitHub Actions

## Local Development

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## Project Structure

```
/
├── public/
│   └── index.html          # Particle animation landing page
├── src/
│   ├── content/
│   │   └── blog/           # Blog posts in Markdown
│   ├── layouts/
│   │   └── BaseLayout.astro
│   └── pages/
│       ├── about.astro
│       ├── contact.astro
│       ├── blog.astro
│       └── blog/
│           └── [...slug].astro
├── astro.config.mjs
└── package.json
```

## Adding Content

### New Blog Post

Create a new `.md` file in `src/content/blog/`:

```markdown
---
title: "Your Post Title"
description: "Brief description"
date: 2026-01-19
---

Your content here...
```

### New Page

Create a new `.astro` file in `src/pages/`:

```astro
---
import BaseLayout from '../layouts/BaseLayout.astro';
---

<BaseLayout title="Page Title">
  <h1>Page Title</h1>
  <p>Your content here...</p>
</BaseLayout>
```

## Deployment

The site automatically deploys to GitHub Pages when you push to the main/master branch.

GitHub Actions handles:
1. Installing dependencies
2. Building the site
3. Deploying to GitHub Pages

## License

Personal website - all rights reserved.
