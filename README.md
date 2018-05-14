# pyenv-pipenv
This Docker image will scan the Pipfile for a specified python_version, install it via pyenv, and then install the dependancies.

# example usage
``` toml
# Pipfile
[[source]]
url = "https://pypi.org/simple"
verify_ssl = true
name = "pypi"

[packages]

[dev-packages]

[requires]
python_full_version = "3.6.5"
```

``` Dockerfile
# Dockerfile
FROM jamesstidard/pyenv-pipenv

RUN python --version  # Python 3.6.5
```
