# Upstream Update Build Docker Image

This action runs the "automerge" script used to deploy changes from the `default` branch to the `master` branch on Pantheon's upstream repositories (`wordpress`, `drops-7`).

## Usage 
```
name: Automerge
on:
    push:
      branches:
        - default

permissions:
  contents: write

jobs:
  automerge:
    runs-on: ubuntu-latest
    steps:
        - uses: actions/checkout@v4
        - uses: pantheon-systems/upstream-update-build@action
```

## Test

python3 test.py
