<h1 align="center">Hi 👋, I'm Anuj Gangwar</h1>
<h3 align="center">A passionate Developer based in Bengaluru</h3>

<!-- TYPING ANIMATION -->
<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&pause=1000&color=00FF99&center=true&vCenter=true&width=500&lines=Software+Development+Student;Java+%26+Backend+Developer;DSA+Enthusiast;Always+Learning+New+Tech" alt="Typing SVG" />
  </a>
</p>

<!-- SOCIAL LINKS -->
<p align="center">
  <a href="https://linkedin.com/in/YOUR_LINKEDIN_USERNAME" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:YOUR_EMAIL_ADDRESS">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" alt="divider" />

### 👨‍💻 About Me

- 🔭 I’m currently working on building an **Attendance Management System** in Java.
- 🌱 I’m currently exploring **Cyber Security** and mastering **Data Structures & Algorithms**.
- 👯 I’m looking to collaborate on backend projects and open-source contributions.
- 💬 Ask me about **Java, C++, and Database Management (MySQL/MongoDB)**.
- 📫 How to reach me: Connect with me on LinkedIn or drop an email!

<br>

### 🛠️ Tech Stack & Tools

<!-- SLEEK SKILL ICONS -->
<p align="left">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=java,c,cpp,mysql,mongodb,git,github,vscode&theme=dark" alt="My Skills" />
  </a>
</p>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" alt="divider" />

### 📊 GitHub Analytics

<p align="center">
  <!-- DARK THEMED STATS FOR ANUJGANGWAR15 -->
  <img src="https://github-readme-stats.vercel.app/api?username=anujgangwar15&show_icons=true&theme=radical&hide_border=true&bg_color=0D1117" alt="GitHub Stats" width="48%" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=anujgangwar15&theme=radical&hide_border=true&background=0D1117" alt="GitHub Streak" width="48%" />
</p>

<!-- TOP LANGUAGES FOR ANUJGANGWAR15 -->
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=anujgangwar15&layout=compact&theme=radical&hide_border=true&bg_color=0D1117" alt="Top Languages" width="400" />
</p>

<br>

### 🐍 Contribution Graph

<!-- SNAKE ANIMATION (Requires GitHub Actions Setup to update dynamically) -->
name: Generate Snake Animation

on:
  # Run automatically every 24 hours
  schedule:
    - cron: "0 0 * * *" 
  
  # Allow manual trigger
  workflow_dispatch:
  
  # Run on every push to the master/main branch
  push:
    branches:
    - main
    - master

jobs:
  generate:
    permissions: 
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5
    
    steps:
      # Step 1: Generate the snake animation files
      - name: Generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: anujgangwar15
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      # Step 2: Push the generated files to the "output" branch
      - name: Push to output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
