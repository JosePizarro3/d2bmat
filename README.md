
<h4 align="center">

[![CI Status](https://github.com/JosePizarro3/d2bmat/actions/workflows/actions.yml/badge.svg)](https://github.com/JosePizarro3/d2bmat/actions/workflows/actions.yml/badge.svg)
[![Coverage](https://coveralls.io/repos/github/JosePizarro3/d2bmat/badge.svg?branch=main)](https://coveralls.io/repos/github/JosePizarro3/d2bmat/badge.svg?branch=main)
<!-- [![PyPI versions](https://img.shields.io/pypi/v/d2bmat)](https://img.shields.io/pypi/v/d2bmat)
[![Python supported versions](https://img.shields.io/pypi/pyversions/d2bmat)](https://img.shields.io/pypi/pyversions/d2bmat) -->

</h4>

`d2bmat` is a Python package with a set of utility functions to map Python schemas and parsers between 2 different database platforms. Its development is strongly tied to Materials Science databases, and as an example, we mainly worked in a mapping between [NOMAD](https://nomad-lab.eu/nomad-lab/) and [openBIS](https://openbis.ch/).

The main objective of this repository is to provide an interface for database admins so that researchers only focus on creating schemas and parsers in **one** common notation, without having to worry about one or another database languages.

If you want to install it, do:
```sh
pip install d2bmat
```

**Note**: the package is still in development and we did not deploy any version to PyPI. If you want to install this package, you need to clone and pip install it locally.

## Development

If you want to develop locally this package, clone the project and enter in the workspace folder:

```sh
git clone https://github.com/JosePizarro3/d2bmat.git
cd d2bmat
```

Create a virtual environment (you can use Python>3.9) in your workspace:

```sh
python3 -m venv .venv
source .venv/bin/activate
```

And run the following commands:
```sh
pip install --upgrade pip
pip install uv
uv pip install -e '.[dev]'
```

### Run the tests

You can locally run the tests by doing:

```sh
python -m pytest -sv tests
```

where the `-s` and `-v` options toggle the output verbosity.

You can also generate a local coverage report:

```sh
python -m pytest --cov=src tests
```

### Run auto-formatting and linting

We use [Ruff](https://docs.astral.sh/ruff/) for formatting and linting the code following the rules specified in the `pyproject.toml`. You can run locally:

```sh
ruff check .
```

This will produce an output with the specific issues found. In order to auto-fix them, run:

```sh
ruff format . --check
```

If some issues are not possible to fix automatically, you will need to visit the file and fix them by hand.


## Main contributors

The main code developers are:

| Name                | E-mail                                                       |
| ------------------- | ------------------------------------------------------------ |
| Dr. Jose M. Pizarro | [jose.pizarro-blanco@bam.de](mailto:jose.pizarro-blanco@bam.de) |
