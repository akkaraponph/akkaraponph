name: Waka Readme

on:
  workflow_dispatch: # for manual workflow trigger
  schedule:
    - cron: '30 14 * * *' # runs at every 12AM UTC

jobs:
  update-readme:
    name: WakaReadme DevMetrics
    runs-on: ubuntu-latest
    steps:
      - uses: guilyx/waka-readme@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          GH_TOKEN: ${{ secrets.BD_TOKEN }}
          SECTION_NAME: "waka-simple"
          COMMIT_MESSAGE: "build: updated simple waka stats section"
          BLOCKS: "⣀⣄⣤⣦⣶⣷⣿"
          TIME_RANGE: all_time
          SHOW_TIME: true
          SHOW_MASKED_TIME: true
          SHOW_TITLE: true
          SHOW_OS: "False"
          SHOW_PROJECTS: "True"
          SHOW_UPDATED_DATE: "True"
          SHOW_PROFILE_VIEWS: "False"
          SHOW_EDITORS: "False"
          SHOW_LANGUAGE: "True"
          SHOW_LANGUAGE_PER_REPO: "False"
          SHOW_LINES_OF_CODE: "True"
          SHOW_COMMIT: "True"
          SHOW_LOC_CHART: "False"
          SHOW_DAYS_OF_WEEK: "False"
          SHOW_SHORT_INFO: "True"
    
