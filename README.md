## Hi there 👋

- 🛠  I’m currently working on Python automation projects
- 📘 I’m currently learning better Python practices and code optimization
- 🤝 I’m looking to collaborate on open source Python projects
- 🧠 I’m looking for guidance on scalable and maintainable applications
- 💬 Ask me about Python and automation
- ⚡ Fun fact:  I’m always looking for ways to make my code more efficient and practical
  

<img alt="Python" height="40" width="50"
     src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
<img alt="GitHub" height="40" width="50"
src="https://raw.githubusercontent.com/devicons/devicon/master/icons/github/github-original.svg">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/david-ferreira-b324a71a3)
[![iCloud Mail](https://img.shields.io/badge/iCloud_Mail-1C1C1E?style=for-the-badge&logo=apple&logoColor=white)](mailto:davidfsillva@icloud.com)

![GitHub Streak](https://streak-stats.demolab.com?user=davidfsillva&theme=dark)

name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"   # todo dia
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: davidfsillva
          outputs: |
            dist/github-contribution-grid-snake.svg
      - uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
