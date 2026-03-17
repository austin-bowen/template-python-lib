# Contributing

## Setup

After cloning the repo, create the virtual environment and install all dependencies:

```bash
uv sync
```

Activate the virtual environment:

```bash
source .venv/bin/activate
```

## Managing Dependencies

### Add a dependency

```bash
uv add [--dev] <package>
```

### Remove a dependency

```bash
uv remove <package>
```

### Update dependencies

Update all dependencies to their latest allowed versions:

```bash
uv sync --upgrade
```

Update a specific dependency:

```bash
uv sync --upgrade-package <package>
```

## Publishing

### First-time setup

Create a `~/.pypirc` file with your PyPI API token:

```ini
[distutils]
index-servers = pypi

[pypi]
username = __token__
password = pypi-<your-token>
```

### Release steps

1. Update the version in `pyproject.toml`
2. Commit and tag the release: `git tag v<version>`
3. Build the package: `bin/build`
4. Publish to PyPI: `bin/publish`
