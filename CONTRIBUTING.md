# Contributing

## Local Checks

Install pre-commit and enable the repository hooks:

```bash
pip install pre-commit
pre-commit install
```

Run the full hook set before opening a pull request:

```bash
pre-commit run --all-files
```

The hooks check for trailing whitespace, missing final newlines, merge conflicts, TOML/YAML syntax, leaked secrets, Rust formatting, and Clippy warnings.
