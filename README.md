Welcome to my GitHub! My name is Gabriela Medeiros.

- Learning always
- Looking for an oportunity

 <div>
  <a href="https://github.com/gabrielamed">
  <img height="170em" src="https://github-readme-stats.vercel.app/api?username=gabrielamed&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true"/>
  <img height="150em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=GabrielaMed&layout=compact&langs_count=7&theme=tokyonight"/>
</div>

##

<div>
 <a href="https://instagram.com/gabrielasmed" target="_blank"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
  <a href = "mailto:gabrielasiqueiramedeiros@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white"></a>
  <a href="https://www.linkedin.com/in/gabriela-siqueira-medeiros-23b83b203/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
</div>

 #snake animation
 
 name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: GabrielaMed
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  
