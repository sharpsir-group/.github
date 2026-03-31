# Brand Assets

Shared logos and banners for all Sharp International Realty repositories.

## Available Assets

| Asset | File | Preview |
|---|---|---|
| Logo (white on transparent) | `logo-white.svg` | For dark backgrounds |
| Logo (dark background) | `logo-dark.svg` | Standalone with dark (#0d1117) background |

## Usage in READMEs

Reference assets via raw URL:

```
https://raw.githubusercontent.com/sharpsir-group/.github/main/brand/FILENAME
```

### Logo on dark background (works in both GitHub light and dark mode)

```markdown
<p align="center">
  <a href="https://sharpsir.group">
    <img src="https://raw.githubusercontent.com/sharpsir-group/.github/main/brand/logo-dark.svg" alt="Sharp International Realty" width="480" />
  </a>
</p>
```

### Logo with GitHub dark/light mode support

```html
<p align="center">
  <a href="https://sharpsir.group">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/sharpsir-group/.github/main/brand/logo-white.svg" />
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/sharpsir-group/.github/main/brand/logo-dark.svg" />
      <img alt="Sharp International Realty" src="https://raw.githubusercontent.com/sharpsir-group/.github/main/brand/logo-dark.svg" width="480" />
    </picture>
  </a>
</p>
```

### Per-repo banner template

Copy and customize `banner-template.svg`, replacing the project name text:

```markdown
<p align="center">
  <img src="https://raw.githubusercontent.com/sharpsir-group/YOUR-REPO/main/.github/banner.svg" alt="Project Name" width="720" />
</p>
```
