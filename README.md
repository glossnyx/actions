## Usage

```yml
name: Deploy

on:
  release:
    types: [published]

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout
        uses: actions/checkout@v2

      - name: Deploy
        uses: glossnyx/deploy-minecraft-mod-action@main
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
```