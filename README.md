# Frequency Analysis on Caesar Cipher

[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/bitnik/analyse-caesar-cipher/main.svg)](https://results.pre-commit.ci/latest/github/bitnik/analyse-caesar-cipher/main)

There are 3 options to run this project.

## Run on Remote

https://bitnik.github.io/analyse-caesar-cipher/

This is a static site powered by [JupyterLite](https://jupyterlite.readthedocs.io/en/stable/) and deployed on [GitHub Pages](https://pages.github.com/).

## Run on Binder

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/bitnik/analyse-caesar-cipher/HEAD?labpath=analyse_caesar_cipher.ipynb)

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
# jupyter lab
jupyter lab analyse_caesar_cipher.ipynb --port 8888
# jupyter notebook
# jupyter notebook analyse_caesar_cipher.ipynb --port 8888
# jupyter notebook --no-browser

# jupyter labextension list
```

Or run JupyterLite server:

```sh
# https://jupyterlite.readthedocs.io/en/stable/quickstart/standalone.html
jupyter lite build --contents content
jupyter lite serve
```
