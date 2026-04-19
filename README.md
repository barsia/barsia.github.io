# Siarhei's Blog

Built with Codocation IDE.

## Getting Started

1. Open the project in Codocation IDE.
2. Edit English pages in `locales/en/pages/`.
3. Update the English navigation and page tree in `locales/en/blog.tree.yml`.
4. Use `codocation.yml` for the site, locale, deployment, and build configuration.

## Structure

```text
.
├── codocation.yml
└── locales/
    └── en/
        ├── blog.tree.yml
        └── pages/
            ├── index.md
            ├── about.md
            └── posts/
```

Each locale has its own directory under `locales/`, with a locale-specific `blog.tree.yml` and Markdown pages. Published pages are registered in that locale's tree; draft posts remain absent from the tree until publication.

## Learn More

Visit [Codocation Documentation](https://codocation.com/docs) for more information.
