# HelloActions

[![Dev Branch](https://github.com/mrprajesh/HelloActions/actions/workflows/dev.yml/badge.svg)](https://github.com/mrprajesh/HelloActions/actions/workflows/dev.yml)
[![Main Branch](https://github.com/mrprajesh/HelloActions/actions/workflows/main.yml/badge.svg)](https://github.com/mrprajesh/HelloActions/actions/workflows/main.yml)

### Steps to create badge for dev branch

**IMPORTANT:** Replace `dev`, `<username>` and `<repo>` with approprite names.
Should be able to see the badge on GitHub.

1. Repo create or use exiting one.
2. git clone repo
3. Switch/checkout to `dev` branch
4. mkdir -p .github/workflows && cd .github/workflows
5. create `dev.yml` as we are creating a badge for `dev` branch. 
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
5. Update `Readme.md` with the below.
 ```
 [![Dev Branch](https://github.com/<username>/<repo>/actions/workflows/dev.yml/badge.svg)](https://github.com/<username>/<repo>/actions/workflows/dev.yml)
 ```
6. git add & commit!
7. git push origin dev 

