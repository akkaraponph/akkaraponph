name: generate monkeytype readme svg

on:
    schedule:
      - cron: "0 */12 * * *"
    workflow_dispatch:

jobs:
    download-svg:
        runs-on: ubuntu-latest

        steps:
            - name: Checkout code
              uses: actions/checkout@v4

            - name: Set up Node.js
              uses: actions/setup-node@v3
              with:
                  node-version: "20.x"

            - name: Generate Monkeytype Readme SVG
              uses: monkeytype-hub/monkeytype-readme@v1.0.0
              with:
                  username: akkaraponph
                  themes: nord_light
                  target-branch: akkaraponph-
                  github-token: ${{ secrets.GH_TOKEN }}