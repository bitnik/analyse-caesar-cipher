# Frequency Analysis on Caesar Cipher

[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/bitnik/analyse-caesar-cipher/main.svg)](https://results.pre-commit.ci/latest/github/bitnik/analyse-caesar-cipher/main)

There are 3 options to run this project.

## Run on Remote

https://bitnik.github.io/analyse-caesar-cipher/lab/index.html?path=analyse_caesar_cipher.ipynb

This is a static site powered by [JupyterLite](https://jupyterlite.readthedocs.io/en/stable/)
(using [pyodide](https://pyodide.org/en/stable/) kernel)
and deployed on [GitHub Pages](https://pages.github.com/).

**Important**: All changes you make there, they will be stored in browser storage.
If you want to revert all changes, you should clear the site data in your browser.

## Run on Binder

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/bitnik/analyse-caesar-cipher/HEAD?labpath=notebooks%2Fanalyse_caesar_cipher.ipynb)

By clicking the badge above, you can run this project on [mybinder.org](https://mybinder.readthedocs.io/en/latest/).

## Run locally

Install dependencies:

```sh
pip install pip-tools
pip-compile -o requirements.txt pyproject.toml
pip-compile --extra dev -o dev-requirements.txt pyproject.toml
pip-sync requirements.txt dev-requirements.txt
```

Run jupyter lab server:

```sh
# Disable classic notebook view
jupyter server extension disable nbclassic
# Run jupyter lab
jupyter lab notebooks/analyse_caesar_cipher.ipynb --port 8888

# jupyter server extension list
# jupyter labextension list
```

Or run JupyterLite server:

```sh
# https://jupyterlite.readthedocs.io/en/stable/quickstart/standalone.html
jupyter lite build
jupyter lite serve --port 8889
```
