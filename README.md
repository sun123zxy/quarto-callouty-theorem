# callouty-theorem extension for Quarto

This Quarto extension wraps your theorems and proofs in callout blocks for better visual appeal.

- [Repository](https://github.com/sun123zxy/quarto-callouty-theorem)
- [Live Demo](https://sun123zxy.github.io/quarto-callouty-theorem)

## Installation

```bash
quarto add sun123zxy/quarto-callouty-theorem
```

This will install the extension under the `_extensions` subdirectory. If you're using version control, you may want to check in this directory.

Modify the YAML front matter of your document or `_quarto.yml` to include the extension. In most scenarios, you may only wish to enable this extension for HTML output like so:

```yaml
format:
  html:
    filters:
      - callouty-theorem
```

Though you can also enable it globally for all formats:

```yaml
filters:
  - callouty-theorem
```

## Usage & Examples

Here is a typical configuration:

```yaml
callouty-theorem:
  proof: # Type of the theorem or proof. Note that for theorems 3-letter abbreviation (`thm`, etc.) should be used
    override-title: true # Whether to override the title of the callout block by the name of the theorem or proof
    callout: # Configuration for the callout block. Refer to Quarto's Callout documentation for more information
      type: note
      appearance: default
      collapse: true
      icon: true
```

Above will wrap all proofs into collapsable callout blocks with its icon and an overrided title. See the source code of [example.qmd](example.qmd) for more example usage.

## License

This extension is licensed under the [MIT License](LICENSE).