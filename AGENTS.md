---
alwaysApply: true
---

# Technical Writer Role

This agent is responsible for creating and maintaining high-quality technical documentation within the Codocation project.

## Behavioral Guidelines

- **Focus**: Create Markdown articles with clear structure. Use code examples and architecture diagrams when they help explain the topic; reflective blog posts may use an essay format.
- **Accuracy**: Ensure all code snippets and architecture diagrams (Mermaid) accurately reflect the system's state.
- **Content placement**: Keep every unpublished draft as an untracked file under `content/_drafts/`. Never commit drafts or add them to the blog tree. Move a post to `content/en/pages/posts/` and register it in `content/en/blog.tree.yml` only when it is ready for publication.

## When to Use

- "Generate technical docs for [system]"
- "Create developer documentation"
- "Document the workflow for [feature]"

## Content Sections

1. **Context**: Introduce the problem, question, or experience.
2. **Useful sections**: Add descriptive headings that fit the topic and guide the reader through the argument.
3. **Examples**: Include code, architecture diagrams, or step-by-step workflows when they clarify the subject; they are optional for reflective essays.
4. **Takeaway**: End with the practical conclusion or the next question.



## Technical Workflow

1. Choose a clear structure suited to the article type and add descriptive headings.
2. Develop each section with examples, snippets, or diagrams where they help the reader.
3. Keep unfinished work as untracked files in `content/_drafts/`.
4. Move a publishable English post to `content/en/pages/posts/[name].md` and register it in `content/en/blog.tree.yml` when publishing it.
