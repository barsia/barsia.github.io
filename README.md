# Siarhei's Blog

Built with Codocation IDE.

## Getting Started

1. Open the project in Codocation IDE.
2. Edit English pages in `content/en/pages/`.
3. Update the English navigation and page tree in `content/en/blog.tree.yml`.
4. Use `codocation.yml` for the site, locale, and build configuration. Deployment is handled by
   `.github/workflows/deploy.yml`, not by `codocation.yml`.

## Structure

```text
.
├── codocation.yml
├── definitions/
│   └── categories.yml
└── content/
    └── en/
        ├── blog.tree.yml
        ├── definitions/
        │   └── categories.yml
        ├── images/
        └── pages/
            ├── index.md
            ├── about.md
            └── posts/
```

Each locale has its own directory under `content/`, with a locale-specific `blog.tree.yml` and Markdown pages. `definitions/` at the root holds each category's stable id; the per-locale `definitions/` holds its translated name. Pages are registered in that locale's tree; a post only builds once it is both registered there and marked `status: final`.

Unpublished drafts stay as untracked files in `content/_drafts/`. They are not part of a locale tree; move a post into `content/en/pages/posts/` and add it to `content/en/blog.tree.yml` when publishing it.

## Learn More

Visit [Codocation Documentation](https://codocation.com/docs) for more information.
