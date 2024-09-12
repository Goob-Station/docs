# Goob Station Docs

This is the `mdbook`-based developer documentation for Goob Station. These docs cover many topics and can be potentially very useful for mappers, spriters, active contributors, & prospective contributors.

The site is currently hosted at [https://docs.goobstation.com](https://docs.goobstation.com).

Benefits of the current docs site infrastructure include:
- First-class git support, open source and actually editable by everyone
- Decently familiar & comfortable for developers since `mdbook` use is very widespread
- No sign-on infrastructure or hosting necessary (besides GH pages), if forks would like to host their own
- Very low friction to adding new pages and editing/fixing old ones
- High level of customizability with styling and easy custom scripting
- Eventual localization support

The following `mdbook` features & plugins are available and in use:
- `MathJax` support 
- Sidebar ToC (integrated directly into `index.hbs` etc)
- `mdbook-mermaid`
- `mdbook-linkcheck`
- `mdbook-template`
- `mdbook-admonish`
- `mdbook-emojicodes`

**For information such as how to edit, build & test these docs, see [Guide to Editing Docs](https://docs.goobstation.com/en/meta/guide-to-editing-docs.html). on the site itself** (or [in this repo](./src/en/meta/guide-to-editing-docs.md))

## License

The Goob Station Docs are released under the Mozilla Public License v2.0.
