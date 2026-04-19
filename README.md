# Siarhei's Blog

Built with Codocation IDE.

## Getting Started

1. Open the project in Codocation IDE
2. Edit content in `content/topics/`
3. Use the Codocation tool windows (TOC, Preview, Site & Export)
4. Export a site (ZIP) or PDF, then deploy/share

## Structure

```
blog/
├── codocation.xml          # Module config and instances
├── content/
│   ├── blog.tree.xml       # Table of contents: header, toc, footer
│   ├── topics/             # Markdown content files (default locale)
│   ├── images/             # Image assets
│   └── snippets/           # Reusable code snippets
├── resources/
│   ├── variables.xml       # Reusable variables
│   ├── labels.xml          # Content labels/tags
│   ├── glossary.xml        # Glossary terms
│   └── keymaps.xml         # Keyboard shortcuts and mappings
└── build/                  # Generated output (created on build, ignored by git)
```

## Advanced: Nested Folders

For larger projects, you can organize topics in subfolders:

```
content/
└── topics/
    ├── index.md
    ├── getting-started/
    │   ├── installation.md
    │   └── quickstart.md
    └── guides/
        ├── basics.md
        └── advanced/
            └── customization.md
```

Reference nested topics in `blog.tree.xml`:
```xml
<topic file="getting-started/installation.md"/>
```

## Learn More

Visit [Codocation Documentation](https://codocation.com/docs) for more information.
