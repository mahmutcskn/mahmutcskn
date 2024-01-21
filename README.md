![visitor badge](https://visitor-badge.laobi.icu/badge?page_id=jwenjian.visitor-badge)
<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Roboto&size=40&pause=1000&center=true&vCenter=true&random=false&width=1000&height=100&lines=Hi+There+👋;I'm+Mahmut!" alt="Typing SVG" /></a>
<hr>
</hr>
<p>
  <h3 align=center>
    A passionate software developer
  </h3>
  <div align=center>
    - 🔭 I’m currently working on ASP.NET Core
  </div>
  <div align=center>
    - 🌱 I’m currently learning C#
  </div>
  <div align=center>
    - 🤔 I’m looking for help with C#
  </div>
  <div align=center>
    - 📫 How to reach me: mahmutcoskunmailbox@gmail.com
  </div>
  <div align=center>
    - 😄 Pronouns: he/him
  </div>
  <div align=center>
    - ⚡ Fun fact: I love spend my free time on learning cyber security
  </div>
  <br>
</p>
<div align=center>
  <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" />

  <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
</div>
<hr>
</hr>
<h2 align=center>
    ⚒️ Languages-Frameworks-Tools ⚒️
  </h2>
  <br>
<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=js,html,css,cs,dotnet,git,github" />
  </a>
</p>
<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=py,raspberrypi,tensorflow,unity,unreal,visualstudio,vscode,wordpress" />
  </a>
</p>
<br>
<hr>
</hr>
  <h2 align=center>
    🐍 My Contributions 🐍
  </h2>
  <div align=center>
    <a href="https://git.io/streak-stats"><img src="https://streak-stats.demolab.com?user=ctrlActrlV&theme=transparent&border_radius=9" alt="GitHub Streak" /></a>
  </div>
  
[![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=ctrlActrlV)](https://github.com/ctrlActrlV/github-readme-stats)

<div>
  <a href="https://github.com/anuraghazra/github-readme-stats">
  <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=anuraghazra&repo=github-readme-stats" />
</a>
<a href="https://github.com/anuraghazra/convoychat">
  <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=anuraghazra&repo=convoychat" />
</a>
</div>

<div>
  <a href="https://github.com/anuraghazra/github-readme-stats">
  <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=anuraghazra&repo=github-readme-stats" />
</a>
<a href="https://github.com/anuraghazra/convoychat">
  <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=anuraghazra&repo=convoychat" />
</a>
</div>




# GitHub Action for generating a contribution graph with a snake eating your contributions.
name: Generate Snake

# Controls when the action will run.
on:
  schedule:
      # every 12 hours
    - cron: "0 */12 * * *"

  # This command allows us to run the Action automatically from the Actions tab.
  workflow_dispatch:
  
  # Also run on every push on the master branch
  push:
    branches:
    - main

# The sequence of runs in this workflow:
jobs:
  # This workflow contains a single job called "build"
  build:
    # The type of runner that the job will run on
    runs-on: ubuntu-latest


    # Steps represent a sequence of tasks that will be executed as part of the job
    steps:
      - name: Clone repo
        uses: actions/checkout@v3
    
      - name: Generate the snake files in './dist/'
        uses: Platane/snk@v3
        id: snake-gif
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
            dist/github-contribution-grid-snake.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9
        env:
           GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

      - name: Show build status
        run: git status

      - name: Push new files to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
          commit_message: Update snake animations
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}




<!--
**ctrlActrlV/ctrlActrlV** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:
<div>
    <a href="https://github.com/ctrlActrlV/github-readme-stats">
      <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=ctrlActrlV&repo=github-readme-stats" />
    </a>
    <a href="https://github.com/ctrlActrlV/convoychat">
      <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=ctrlActrlV&repo=convoychat" />
    </a>
</div>

[![GitHub Streak](https://streak-stats.demolab.com/?user=ctrlActrlV)](https://git.io/streak-stats)  


- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

  [![My Skills](https://skillicons.dev/icons?i=js,html,css,cs,dotnet,git,github,py,raspberrypi,tensorflow,unity,unreal,visualstudio,vscode,wordpress)](https://skillicons.dev)


[![GitHub Streak](https://streak-stats.demolab.com/?user=DenverCoder1&theme=dark)](https://git.io/streak-stats)

[![My Skills](https://skillicons.dev/icons?i=js,html,css,cs,dotnet,git,github,py,raspberrypi,tensorflow,unity,unreal,visualstudio,vscode,wordpress)](https://skillicons.dev)

[![Typing SVG](https://readme-typing-svg.demolab.com/?lines=Hi+There;My+name+is+Mahmut)](https://git.io/typing-svg)
-->
