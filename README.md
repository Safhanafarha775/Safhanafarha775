# Hello World 👋, I'm Safhana!
🌟 Aspiring Data Scientist & Robotics Enthusiast  
💻 Passionate about AI, Robotics, and Problem-Solving  
📍 From India, dreaming to work abroad (Dubai, Qatar, Sharjah)  

## 🚀 Skills & Tools
- Python 🐍 | Data Science 📊 | AI 🤖 | Robotics 🔧  
- SQL | Machine Learning | Deep Learning | Computer Vision  
- Tools: GitHub, Jupyter, Arduino, Scratch  

## 🔗 Connect with me
- 🌐 Portfolio : https://sites.google.com/view/safhanafarha/home  
- 💼 LinkedIn : www.linkedin.com/in/safhanafarha786  
- 📧 Email: safhanafarha775@gmail.com  


name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"  # Runs every day at midnight
  workflow_dispatch:      # Allow manual run

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: SafhanaFarhath   # replace with your GitHub username
          outputs: dist/snake.svg

      - name: Push to output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

![GitHub Snake Light](https://raw.githubusercontent.com/SafhanaFarhath/SafhanaFarhath/output/snake.svg#gh-light-mode-only)
![GitHub Snake Dark](https://raw.githubusercontent.com/SafhanaFarhath/SafhanaFarhath/output/snake.svg#gh-dark-mode-only)



