# Testing

***************************************************************************

Testing is a critical aspect of software development to ensure the reliability and functionality of the backend of the Compax web app. Below are the blocks of code for testing compax api:

## pytest

```python

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

permissions:
  contents: read

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
    - name: Set up Python 3.10
      uses: actions/setup-python@v3
      with:
        python-version: "3.10"
    - uses: actions/cache@v3
      id: cache
      with:
        path: ~/.cache/pip
        key: ${{ runner.os }}-pip-${{ hashFiles('**/requirements.*') }}
        restore-keys: | 
          ${{ runner.os }}-pip-
    - name: Install dependencies
      run: |
        python -m pip install --upgrade pip
        pip install -r requirements.txt        
    - name: Run pytest
      run: | 
        pytest
```