# HelloActions

[![Dev Branch](https://github.com/mrprajesh/HelloActions/actions/workflows/dev.yml/badge.svg)](https://github.com/mrprajesh/HelloActions/actions/workflows/dev.yml)
[![Main Branch](https://github.com/mrprajesh/HelloActions/actions/workflows/main.yml/badge.svg)](https://github.com/mrprajesh/HelloActions/actions/workflows/main.yml)

### Steps
1. Repo create or exits.
2. Clone repo
3. mkdir -p .github/workflows && cd .github/workflows
4. create dev.yml
```
name: Dev Branch

on:
  push:
    branches: [ dev ]
  pull_request:
    branches: [ dev ]

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
    - name: make
      run: make
```
5. Update Readme as 
 ```
 [![Dev Branch](https://github.com/<username>/<repo>/actions/workflows/dev.yml/badge.svg)](https://github.com/<username>/<repo>/actions/workflows/dev.yml)
 ```
6. Git add & commit!
7. Git push. 
