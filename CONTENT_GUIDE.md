# Content Guide

This guide explains how to add new content to the site.

## Quick Start

Use Hugo's `new` command with the appropriate archetype:

```bash
# Create a new blog post
hugo new blog/my-new-post.md

# Create a new talk
hugo new talks/my-conference-talk.md

# Create a new podcast appearance
hugo new podcasts/my-podcast-episode.md

# Create a new project
hugo new projects/my-project.md
```

## Content Types

### Blog Posts

Location: `content/blog/`

```yaml
---
title: "My Blog Post Title"
date: 2024-01-15
tags:
  - go
  - tutorial
summary: "A brief description shown on list pages (2-3 sentences)"
featured: false
draft: false
---
```

**Fields:**
- `title`: Post title
- `date`: Publication date (YYYY-MM-DD)
- `tags`: Array of tags for categorization
- `summary`: Short excerpt shown on list pages (2-3 sentences)
- `featured`: Set to `true` to highlight on homepage
- `draft`: Set to `true` while working on the post

### Talks

Location: `content/talks/`

```yaml
---
title: "My Talk Title"
date: 2024-01-15
event: "Conference Name 2024"
location: "City, Country"
summary: "Brief description of the talk"
tags:
  - go
  - tinygo
slides_url: "https://link-to-slides.com"
video_url: "https://youtube.com/watch?v=xxxxx"
featured: true
source_post: "/blog/my-related-post/"
---
```

**Fields:**
- `event`: Conference or meetup name
- `location`: Where the talk was given
- `slides_url`: Link to slides (Google Slides, Speaker Deck, GitHub, etc.)
- `video_url`: Link to video recording (YouTube, Vimeo, etc.)
- `source_post`: Optional link to a related blog post

### Podcasts

Location: `content/podcasts/`

```yaml
---
title: "Episode Title"
date: 2024-01-15
podcast: "Podcast Name"
summary: "Brief description of the episode"
tags:
  - go
  - interview
episode_url: "https://link-to-episode.com"
featured: false
source_post: "/blog/my-related-post/"
---
```

**Fields:**
- `podcast`: Name of the podcast
- `episode_url`: Link to listen to the episode
- `source_post`: Optional link to a related blog post

### Projects

Location: `content/projects/`

```yaml
---
title: "Project Name"
date: 2024-01-15
role: "Creator"
summary: "Brief description of the project"
tags:
  - go
  - opensource
repo_url: "https://github.com/username/repo"
website_url: "https://project-website.com"
featured: true
source_post: "/blog/my-related-post/"
---
```

**Fields:**
- `role`: Your role in the project (Creator, Contributor, Co-Author, etc.)
- `repo_url`: Link to the source code repository
- `website_url`: Link to the project website
- `source_post`: Optional link to a related blog post

## Featured Content

To feature content on the homepage, set `featured: true` in the frontmatter.

The homepage displays:
- Latest 3 blog posts (regardless of featured status)
- Featured talks (or latest 3 if none featured)
- Featured podcasts (or latest 2 if none featured)
- Featured projects (or latest 3 if none featured)

## Adding Images

For blog posts, use page bundles:

```
content/blog/my-post/
├── index.md
├── image1.png
└── image2.jpg
```

Reference images in your markdown:
```markdown
![Alt text](image1.png)
```

## Publishing

1. Create your content with `draft: true`
2. Preview locally with `hugo server -D`
3. When ready, set `draft: false`
4. Commit and push to deploy

## Local Development

```bash
# Start development server (includes drafts)
hugo server -D

# Build the site
hugo

# Build with minification
hugo --minify
```

## Achievements

Achievements are managed in `data/achievements.yaml`:

```yaml
items:
  - title: "Achievement Title"
    description: "Description of the achievement"
    year: "2024"
    icon: "🏆"
```

## Need Help?

Check the [Hugo documentation](https://gohugo.io/documentation/) or open an issue on the repository.
