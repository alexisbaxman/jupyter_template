# Jupyter Book Template Manual

There are several workflows to create and work with Jupyter Book:
* **Canonical Jupyter Book workflow:** as described in the official Jupyter Book documentation, it requires to locally install Jupyter Book (via pip or conda-forge), initialiding a MyST project and use command line to build the book from local stored markdown files. This is the most standard approach and is useful for local preview.
* **GitHub direct workflow:** This is the workflow used for the MEGqc and BIDS-Manager documentation, and the one described in this protocol. You can create and edit your book by editing the repository files directly in GitHub, while GitHub Actions handles the building and deployment of the website. This workflow allows you to work remotely from the browser, without a local environment, without an installed CLI. 

*This repository allows you to clone it and start your own documentation by editing the existing files right away. The pictures in this protocol are stored in the folder `pics`, which you can safely erase. The images are taken from the BIDS-Manager documentation.*


## How to start:
The quickest approach is to clone an existing documentation repository that already compiles and deploys successfully, and then edit the different files to fit your needs. This repository contains the essential files and structure needed to build and deploy a Jupyter Book.

* `README.md`: This Markdown file defines the description shown on a repository's front page, such as the protocol you are currently reading. It follows standard Markdown rules (explained below). Feel free to modify it.

* `_toc.yml`: This YAML file defines the Jupyter Book structure, such as which pages (Markdown files) are included, their order and hierarchy. The pages are divided in `chapters` (top-level pages) and `sections` (nested pages under a chapter). The `_toc.yml` references each page by its relative path without the .md extension. In the example below you can see how:
  * Pages 4 and 5 (`sections`) are nested pages under page 3 (`chapter`).
  * The order and hierarchy will be reflected in the compiled Jupyter Book's left navigation panel.
  * It's recommended to keep the pages organized in folders (e.g., content/, section/). 
  
<img src="./static/pics/toc.png" alt="toc" width="650px" align="center">

<br>


* `index.md`: by convention, "index.md" is the filename use for the welcome page of the Jupyter Book. It typically includes a brief overview of what the documentation is for, who it is intended for (e.g., beginners vs. advanced users), any prerequisites (e.g., Python, required software, background knowledge), links for support (e.g., contact email, GitHub Issues), and optional sections such as acknowledgements or citations.

<img src="./static/pics/index.png" alt="index" width="550px" align="center">

<br>

* `_config.yml`: This YAML file customizes some metadata elements of the Jupyter Book's such as title, author and logo. The book can still build without this file, but it's highly recommended to have a basic customization. The `_config.yml` file in this repository is quite basic, but many advance functions and settings are available, check the [Jupyter Book Configuration reference page](https://jupyterbook.org/v1/customize/config.html).

<img src="./static/pics/config.png" alt="toc" width="650px" align="center">

  * <img src="./static/pics/github_option.jpg" alt="toc" width="250px" align="right"> The  "HTML-specific settings" of the `_config.yml` file allows to turn on the GitHub button in the right-top corner. When hovering, you get quick access to the whole repository, to the edition page and to the issues page.'


  * The "parse > myst_enable_extensions" of the `_config.yml` file is necessary to work with raw HTML images. More about handling HTML images below. 



<br>


* `.github/workflows/deploy.yml`: It includes the key instructions for GitHub Actions that builds the book and published it to GitHub Pages. It activates every time a change happens anywhere in the repository. It installs Jupyter Book and any specified dependencies.  The `deploy.yml` in this repository is reduced to the essential configurations, taken from the official [GitHub Pages and Actions](https://jupyterbook.org/v1/publish/gh-pages.html).


<br>

* `requirements.txt`: A plain text file listing the Python packages required to build the Jupyter Book. During deployment, this file is read by the workflow file (`deploy.yml`), which uses it to `pip` install the specified dependencies. If required packages are missing or incompatible, the book compilation will fail.
   * For a very basic Jupyter Book (like this template), specifying `jupyter-book==1.0.0` in requirements.txt is `sufficient`. However, additional dependencies or specific versions of extensions can be added as needed (for example, `sphinx==7.4.7`). It is also possible to install packages directly in the deployment workflow (`deploy.yml`), but this can lead to conflicts with the dependencies specified in `requirements.txt`.
 
<!--
picture: deploy.yml --> requirements.txt
-->



## Important steps

1. The repository has to be public.
2. This book is built and deployed automatically via **GitHub Actions**.  (In Settings > Pages > Build and deployment: Source: GitHub Actions)
3. If the site doesn’t update, check the **Actions** tab for build logs.
   

## How to compile pictures

* `\static`: the pictures in this ReadMe are stored in the folder `pics`, which you can safely erase, to store your pictures for your Jupyter Book documentation, stored them in the `static` folder).* 
* Boxes
* CheatSheet
* LICENSE  


