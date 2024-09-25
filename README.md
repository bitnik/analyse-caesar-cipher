# Frequency Analysis on Caesar Cipher

[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/bitnik/analyse-caesar-cipher/main.svg)](https://results.pre-commit.ci/latest/github/bitnik/analyse-caesar-cipher/main)

## Run on Binder

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/bitnik/analyse-caesar-cipher/HEAD?labpath=analyse_caesar_cipher.ipynb)

## Development

```sh
pip install pip-tools
pip-compile -o requirements.txt pyproject.toml
pip-compile --extra dev -o dev-requirements.txt pyproject.toml
pip-sync requirements.txt dev-requirements.txt

# jupyter lab
jupyter lab analyse_caesar_cipher.ipynb --port 8888
# jupyter notebook
# jupyter notebook analyse_caesar_cipher.ipynb --port 8888
# jupyter notebook --no-browser
```
