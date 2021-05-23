![Metrics](https://metrics.lecoq.io/alesbabnik?template=classic&languages=1&lines=1&languages.limit=8&languages.colors=github&languages.threshold=0%25&config.timezone=Europe%2FStockholm)

# Visit https://github.com/lowlighter/metrics/blob/master/action.yml for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: alesbabnik
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Europe/Stockholm
          plugin_languages: yes
          plugin_languages_colors: github
          plugin_languages_limit: 8
          plugin_languages_threshold: 0%
          plugin_lines: yes
<!--
**alesbabnik/alesbabnik** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
