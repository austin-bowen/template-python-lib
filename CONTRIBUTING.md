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
