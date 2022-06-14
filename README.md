# setuptools-scm-example

Automatically create version files from git using [`setuptools-scm`](https://github.com/pypa/setuptools_scm/)

## Usage:

Setup virtualenv and install `setuptools-scm`
```python
python -m venv .venv
source .venv/bin/activate
pip install setuptool-scm
```

```python
python -m setuptools_scm # will spit out current version based on git

python print_version.py # prints version programmatically

git commit --allow-empty -m "test commit"
python -m setuptools_scm # version will be 0.1.1.dev1.<revision>.d<date>

git tag -a 0.2.0 -m "release 0.2.0"
python -m setuptools_scm # version will be 0.2.0

git commit --allow-empty -m "first 0.2.1 commit"
python -m setuptools_scm # version will be 0.2.1.dev1.<revision>.d<date>
```
