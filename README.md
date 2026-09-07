# Marco's Utils

Meta package for Marco's Python utilities.

Installing this package installs the utilities listed below directly from their
GitHub repositories.

## Included repositories

- [probdist](https://github.com/marcopettorali/probdist)
- [editplot](https://github.com/marcopettorali/editplot)

## Install with pip

```bash
pip install git+https://github.com/marcopettorali/marcosutils.git
```

From another Python project's `pyproject.toml`:

```toml
dependencies = [
  "marcosutils @ git+https://github.com/marcopettorali/marcosutils.git@main",
]
```

For local development:

```bash
git clone --recurse-submodules https://github.com/marcopettorali/marcosutils.git
cd marcosutils
pip install -e .
```

## Clone

```bash
git clone --recurse-submodules https://github.com/marcopettorali/marcosutils.git
```

If you have already cloned the repo without submodules:

```bash
git submodule update --init --recursive
```

## Update submodules

To update the submodules to the latest commit on their configured branch:

```bash
git submodule update --remote --merge
git commit -am "Update submodules"
```

## Modify the included repositories

The repository list is defined in `.gitmodules` for source checkout and in
`pyproject.toml` for pip installation.

To add a new repository:

```bash
git submodule add https://github.com/owner/repo.git repo
```

Then add the corresponding dependency to `pyproject.toml`:

```toml
dependencies = [
  "repo @ git+https://github.com/owner/repo.git@main",
]
```
