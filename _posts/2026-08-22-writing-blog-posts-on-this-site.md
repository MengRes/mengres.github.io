---
layout: post
title: Writing blog posts on this site
date: 2026-08-22 12:00:00 -0500
description: A starter example for the Blog section — copy this file, rename it, and replace the content with your own notes.
tags: meta al-folio jekyll
categories: notes
related_posts: false
giscus_comments: false
---

This is a **sample post** to show how the Blog section works. You can keep it as a reference, edit it, or delete it once you add your own articles.

## File naming

Create a new file under `_posts/` with this pattern:

```text
YYYY-MM-DD-your-slug.md
```

For example: `2026-09-01-domain-shift-in-pathology.md`.

## Front matter

Each post starts with YAML front matter between `---` lines. Useful fields:

```yaml
---
layout: post
title: Your post title
date: 2026-09-01 10:00:00 -0500
description: One sentence shown on the blog index page.
tags: medical-imaging machine-learning
categories: notes
related_posts: true
giscus_comments: false
---
```

- **description** — summary on `/blog/`
- **tags** — used for related posts (see `_config.yml` → `related_blog_posts`)
- **related_posts: false** — hide the “related posts” block on this page only

## Markdown body

Write the article in Markdown below the front matter.

### Code

```python
import torch

model = torch.hub.load("repo", "model_name")
logits = model(images)
```

### Math

Inline: $E = mc^2$. Display math:

$$
\mathcal{L} = \frac{1}{N} \sum_{i=1}^{N} \ell\bigl(f(x_i), y_i\bigr)
$$

(Math requires `enable_math: true` in `_config.yml`, which is already on.)

### Links and images

- Link to a paper: [MIDL 2026]({{ '/publications/' | relative_url }})
- Add an image: `![caption]({{ '/assets/img/prof_pic.jpg' | relative_url }})`

## Publish

1. Save the file in `_posts/`
2. Commit and push — GitHub Actions deploys to [mengres.github.io](https://mengres.github.io)
3. Open `/blog/` to see the new entry

Replace this placeholder with notes on projects, experiments, or tutorials when you are ready.
