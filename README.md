# demo_uv

UV is built by Astral and written in Rust.
https://github.com/astral-sh/uv

Designed to replace tools like:
- pip
- virtualenv
- poetry
- pyenv

Supports: 
- requirements.txt
- pyproject.toml


# Installation
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Check the version of uv
```bash
uv --version
```
# Applications
Create an application project. 

This creates the following files:
- pyproject.toml
- main.py
- Readme.md
- .python-version

```bash
uv init example-app
```

Execute python file with:
```bash
cd example-app
uv run main.py
```

# Packaged Applications
Use `--package` to create a packaged application. 

Used if publishing to PyPI. Source code is placed in `src` directory.
```bash
uv init --package example-pkg
```

Execute command with:
```bash
cd example-pkg
uv run example-pkg
```

# Libraries
Use --lib to create a library. 

Intended to be built and distributed. A `py.typed` placeholder is included to indicate consumers that types can be read from the library
```bash
uv init --lib example-lib
```

Import and execute library with `uv run`:
```bash
cd example-lib
uv run python -c "import example_lib; print(example_lib.hello())"
```

Creating a virtual environment
```bash
uv venv
```
