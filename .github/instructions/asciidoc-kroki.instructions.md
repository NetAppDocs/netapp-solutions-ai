---
name: AsciiDoc Kroki diagrams
description: Use when editing AsciiDoc pages with Mermaid or other Kroki-rendered diagrams, especially when the task mentions asciidoc.extensions.enableKroki.
applyTo: "**/*.adoc"
---

# AsciiDoc diagrams

- Use the existing diagram form: `[source,mermaid]` followed by a delimited source block. Keep diagram syntax compatible with the cloud documentation renderer.
- Treat `asciidoc.extensions.enableKroki` as a rendering-infrastructure concern. Do not add it to `project.yml` or invent local build configuration; publishing and validation occur in the cloud pipeline described in [README.md](../../README.md).
- Before adding a diagram, inspect nearby pages for the established section structure, terminology, and diagram style. Prefer Mermaid for diagrams already represented as source blocks in this repository.
- Keep explanatory prose immediately before the diagram, state what the reader should learn from it, and ensure labels use the product names and terminology used by the surrounding page.
- Preserve required AsciiDoc frontmatter and page attributes when editing a page. In particular, keep the page permalink aligned with its directory and filename and preserve image/path conventions.
- Avoid changing navigation or site configuration for a diagram-only edit. The site-level settings live in [project.yml](../../project.yml).
- Do not claim that a diagram renders locally unless a repository-provided validation command exists. Cloud publishing is the authoritative rendering check.
