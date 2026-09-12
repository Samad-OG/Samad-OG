# ⚡ `Samad Adil` | Data Science & AI Engineer

```console
$ samad --info
> Status      : B.Tech CSE (Data Science) Student
> Core Focus  : AI/ML Engineering, Predictive Modeling, RAG Architecture
> Location    : Chandigarh, India
> Speciality  : Turning raw data into intelligent, real-world systems
const Developer = {
    languages  : ["Python", "C++", "SQL", "JavaScript"],
    dataScience: ["Machine Learning", "Predictive Modeling", "RAG Architecture", "Data Analysis"],
    tools      : ["Git", "GitHub", "Jupyter Notebooks", "VS Code"],
    building   : ["AI-powered platforms", "End-to-end ML Pipelines"]
};
RepositoryTech StackOverview🚘 Car-Price-PredictionPython Scikit-LearnEnd-to-end ML pipeline to estimate vehicle market values.🌤️ Weather-ForecastJavaScript APIWeb-based real-time weather tracking application.
name: Generate Snake Animation

on:
  schedule:
    - cron: "0 */12 * * *" 
  workflow_dispatch:
  push:
    branches:
    - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 10
    
    steps:
      - name: generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
            
      - name: push github-contribution-grid-snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
