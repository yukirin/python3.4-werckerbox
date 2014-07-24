#python3.4-werckerbox

wercker box

##Usage

wercker.yml for python:
    
```yaml
---
box: yukirin/python3.4-werckerbox@0.1.0

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
