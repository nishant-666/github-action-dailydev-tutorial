# github-action-dailydev-tutorial

# Copy-paste this code

name: DevCard

permissions:
  contents: write

on:
  workflow_dispatch:
  push:
    branches:
      - main
  schedule:
    - cron: "0 0 * * *"

jobs:
  devcard:
    runs-on: ubuntu-latest
    steps:
      - name: devcard
        uses: dailydotdev/action-devcard@2.0.2
        with:
          devcard_id: ${{ secrets.DEVCARD_ID }}
