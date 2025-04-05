from pathlib import Path
import zipfile

# Conteúdo do README.md atualizado com toque fofo
readme_content = """
# 🚀 Bem-vindo(a) ao meu GitHub! 👋

## ૮₍ ´• ˕ •` ₎ა  Um cantinho doce de aprendizado e amor

> 🌸 Bem-vindo(a) ao meu espaço!  
> Aqui é onde compartilho não só códigos, mas também sonhos, conquistas e descobertas.  
> Com o coração de pedagoga e os olhos brilhando pela tecnologia, sigo unindo esses dois mundos com muita dedicação e carinho.  
> Que bom ter você aqui! 💻🌼

---

## 👩‍💻 Olá, eu sou a Erica Lima!

### 📚 Pedagoga | 💻 Estudante de Sistemas de Informação | 🌟 Assessora Acadêmica

Aqui você encontrará projetos que unem minhas duas paixões: **educação** e **tecnologia**. 
Em constante aprendizado, adoro explorar como a tecnologia pode transformar a educação e o mundo ao nosso redor.

---

## 🛠️ Tecnologias que estou explorando

### Linguagens:
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)

### Ferramentas:
![Git](https://img.shields.io/badge/-Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/-GitHub-181717?style=flat-square&logo=github&logoColor=white)
![VS Code](https://img.shields.io/badge/-VS%20Code-007ACC?style=flat-square&logo=visual-studio-code&logoColor=white)

---

## 🌱 Sobre Mim

- 🎓 Formada em **Pedagogia** e estudante de **Sistemas de Informação**.
- 💡 Apaixonada por **tecnologia educacional** e **inovação**.
- 🚀 Buscando unir **educação** e **tecnologia** para criar soluções que transformem vidas.
- ☁️ Acredito que conhecimento compartilhado é uma sementinha de transformação. 🌱

---

## 📊 Estatísticas do GitHub

![Estatísticas do GitHub](https://github-readme-stats.vercel.app/api?username=Ericatech&show_icons=true&theme=radical)
![Linguagens mais usadas](https://github-readme-stats.vercel.app/api/top-langs/?username=Ericatech&layout=compact&theme=radical)

---

## 📊 Contribuições

![Snake animation](https://github.com/Ericatech/Ericatech/blob/output/github-contribution-grid-snake.svg)

---

## 📫 Como me encontrar

- 🌐 [LinkedIn](https://www.linkedin.com/in/érica-lima-santana/)
- 📧 Email: ericalima.santana23@gmail.com

---

⭐️ Feito com ❤️ e muitos sonhos por [Erica Lima](https://github.com/Ericatech)
"""

# Caminhos
readme_path = Path("/mnt/data/README.md")
workflow_dir = Path("/mnt/data/.github/workflows")
workflow_dir.mkdir(parents=True, exist_ok=True)

snake_workflow_content = """
name: Generate Snake Animation 🐍

on:
  schedule:
    - cron: "0 0 * * *"
  push:
    branches:
      - main
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout do repositório
        uses: actions/checkout@v3

      - name: Gera cobrinha animada 🐍
        uses: Platane/snk@v3
        with:
          github_user_name: Ericatech
          outputs: |
            dist/github-contribution-grid-snake.svg

      - name: Commit da cobrinha
        uses: EndBug/add-and-commit@v9
        with:
          author_name: github-actions
          author_email: github-actions@github.com
          message: "Atualiza cobrinha [automático]"
          add: "dist/*.svg"

      - name: Publica no branch output
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_branch: output
          publish_dir: ./dist
"""

workflow_path = workflow_dir / "snake.yml"
readme_path.write_text(readme_content, encoding="utf-8")
workflow_path.write_text(snake_workflow_content, encoding="utf-8")

# Compactar tudo num .zip
zip_path = "/mnt/data/perfil_EricaLima_GitHub.zip"
with zipfile.ZipFile(zip_path, "w") as zipf:
    zipf.write(readme_path, "README.md")
    zipf.write(workflow_path, ".github/workflows/snake.yml")

zip_path


![Estatísticas do GitHub](https://github-readme-stats.vercel.app/api?username=Ericatech&show_icons=true&theme=radical)
![Linguagens mais usadas](https://github-readme-stats.vercel.app/api/top-langs/?username=Ericatech&layout=compact&theme=radical)


---

## 📫 Como me encontrar

- [LinkedIn](https://www.linkedin.com/in/érica-lima-santana/)
- 📧 Email: ericalima.santana23@gmail.com

---

⭐️ Feito com ❤️ por [Erica Lima](https://github.com/Ericatech)

