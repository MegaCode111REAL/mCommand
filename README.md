# mCommand

[![Deploy static content to Pages](https://github.com/MegaCode111REAL/mcommand/actions/workflows/static.yml/badge.svg?branch=main)](https://github.com/MegaCode111REAL/mcommand/actions/workflows/static.yml)

A Minecraft Bedrock command generator powered by a structured `syntax.json` command database.

## GitHub Pages

The site is a static client-side application:

- `index.html` — application interface
- `style.css` — styling and responsive layout
- `app.js` — command loading, argument controls, and command generation
- `syntax.json` — command syntax and type data

No server is required. The app loads `syntax.json` from the repository at runtime.

## Features

- Search the available Bedrock commands.
- Select between multiple documented syntax variants.
- Generate commands from argument controls.
- Use documented enum values when they are present in the data.
- Supports common argument types such as targets, booleans, numbers, effects, and identifiers.
- Copy generated commands directly to the clipboard.
- Works as a GitHub Pages static site.

## Data format

The generator expects `syntax.json` in the repository root. The database can contain command syntax, reusable types, constraints, and statistics.

The frontend is intentionally driven by the data rather than containing a hard-coded list of commands.

## Automatic formatting

This repository includes a reusable GitHub Actions formatter at:

`.github/workflows/format.yml`

On pushes and pull requests, it uses Prettier to format supported files. On pushes to the default branch, changes are committed back automatically using the repository owner's GitHub identity.

The formatter can handle supported JavaScript, TypeScript, HTML, CSS, JSON, Markdown, YAML, and other Prettier-supported formats. Files can be excluded with `.prettierignore`.

## Development

Because this is a static site, you can open `index.html` through a local HTTP server or deploy the repository with GitHub Pages.

For local development, any static web server is sufficient.

## License

See the repository license if one is provided.
