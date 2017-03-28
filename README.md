# python3.4-werckerbox

wercker box

## Usage

wercker.yml for python:
    
```yaml
---
box: yukirin/python3.4-werckerbox@0.2.1

# Build definition
build:
  steps:
    - virtualenv:
        name: setup virtual environment
        python_location: /usr/bin/python3.4

    - pip-install
    - script:
        name: echo python information
        code: |
          echo "python version $(python --version) running"
          echo "pip version $(pip --version) running"
          pip freeze
```

## Licenses
This software is released under the [MIT License][MIT], see LICENSE

[MIT]: http://www.opensource.org/licenses/mit-license.php


## Changelog

### 0.2.1
- Fix typo

### 0.2.0
- Update README

### 0.1.0
- Initial release
