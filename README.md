# Quarto 

El siguiente proyecto es un curso de [nbdev](https://nbdev.fast.ai/). 

**Nbdev**

Es una plataforma de desarrollo de software basado en notebooks que nos permite desarrollar software, hacer limpieza de errores, rehacer código,  generar documentacón de alto nivel, hacer pruebas y mantener una integración continua de forma simple usando notebooks. 


* La documentación del software puede ser generada a partir de simples comandos y puede ser integrada dentro de [Github Pages](https://pages.github.com/). El uso de los notebooks de Markdown nos permite integrar el uso de Latex, esto nos permite generar documentación especializada y hermosa () simples y con el uso 
Documentation is automatically generated using [Quarto](https://quarto.org/) and allows to be hosted using [Github Pages](https://pages.github.com/). The use of notebooks allow the usage of Latex inside the documentation and easy explanation of the code developed.


# 🔦 What is inside this repository 

This repository contains a course of Nbdev

<details><summary><strong>Installation:</strong></summary>

1. Installation anaconda 

2. Installation JupyterLab

3. Installation nbdev

4. Install Quarto

5. Install JupyterLab extension
</details>

<details><summary><strong> How to:</strong></summary>

6. Create a repository.

7. Build the library.

8. Create documentation.  

9. Install package.
</details>

<details><summary><strong>Generate the course:</strong></summary>

Here is a guide of the initial files you want to modify to remove the sections that refer to the template, leaving only what is relevant to developing/updating the material of your course.

1. Start by editing the `README.md` file carefully. 
    - Change the title
    - Remove some of the sections
    - Edit the Dev Setup instructions to cater to your needs.

2. Add your the **course code** and **course name** to the web pages
    - Using the 
    - If you are using VSCode, you can Ctrl + Shift + F (or ⌘ + Shift + F if you are on Mac) and replace all occurrences of `MY_COURSE_CODE` and `MY_COURSE_NAME` to the code and name of your course, respectively.
    - Or, you can manually edit those in the following files:
        - `_quarto.yml`
        - `2023/index.qmd`
        - `helpers/remove-nav.html`
3 To add files to render it has to be on the `_quarto.yml` file. This allows a global control on which files sould be render on the site.

4. Next, modify the content of `index.qmd` and start working properly on your content pages under `2023/*`

5. To generate all the files:

    ```
    quarto preview . --render all --no-browser
    ```
</details>

# 🧰 Dev Setup

On top of the setup below, I also recommend you use [VSCode](https://code.visualstudio.com/Download) as your primary IDE.

<details><summary>🐍 The Python setup</summary>

## 🐍 The Python setup

1. Install [Python 3.8](python.org) or higher on your computer.
2. Install [anaconda](https://www.anaconda.com/products/individual) or [miniconda](https://docs.conda.io/en/latest/miniconda.html) on your computer.
3. Create a new `conda` environment:

    ```bash
    conda create -y -n=venv-my-course python=3.10.8
    ```

    Never worked with conda environments before? Take some time to read [their documentation](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html). 

    💡 **Pro-tip**: replace `my-course` with your course code. Say, for example, `venv-ds105`.

4. Activate the environment and make sure you have `pip` installed inside that environment:

    ```bash
    # the exact `activate` command will vary depending on your OS
    conda activate venv-my-course 
    ```

💡 Remember to activate this particular `conda` environment whenever you reopen VSCode/the terminal.

10. Install required libraries

  ```bash
  pip install -r requirements.txt
  ```

Now, whenever you open a Jupyter Notebook, you should see the `venv-my-course` kernel available.
</details>

<details><summary>📊 The R setup</summary>

<details><summary><img src="https://quarto.org/favicon.png" style="object-fit: cover;width:1em;height:1em;" /> The Quarto setup</summary>

## <img src="https://quarto.org/favicon.png" style="object-fit: cover;width:1em;height:1em;" /> The Quarto setup

1. Install [Quarto](https://quarto.org/docs/getting-started/installation.html) on your computer.
2. Run the following command to start the website locally:

    ```bash
    quarto preview . --render all --no-browser
    ```
    This will read the instructions from `_quarto.yml` and render the website locally.
5. Open your browser and navigate to `http://localhost:<port>/`. That's it!

</details>

<details><summary>🕸️ Publishing the website</summary>

## 🕸️ Publishing the website

I recommend you set up a **GitHub Action** for this. Just follow the instructions in the official [Quarto instructions](https://quarto.org/docs/publishing/github-pages.html#publish-action).

💡 This template already comes with a GitHub workflow setup. You can find it in the [.github/workflows/publish.yml_](.github/workflows/publish.yml_) file. You just need to rename it to `.github/workflows/publish.yml` (remove the underscore at the end)

</details>

# 📟 Contact

**✋ Questions? Suggestions?** If you are not sure how to do something with the template or have a suggestion for a new feature, start a [discussion](https://github.com/jonjoncardoso/quarto-template-for-university-courses/discussions).

**🐞 Spotted any bugs?** Create a new [Issue](https://github.com/jonjoncardoso/quarto-template-for-university-courses/issues).

**🖼️ Want to show us your courses?** Share a link to your public page on the [discussions page](https://github.com/jonjoncardoso/quarto-template-for-university-courses/discussions) or write me an e-mail.