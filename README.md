# Jupyter Book Template Manual

There are several workflows to create and work with Jupyter Book:
* **Canonical Jupyter Book workflow:** as described in the official Jupyter Book documentation, it requires to locally install Jupyter Book (via pip or conda-forge), initialiding a MyST project and use command line to build the book from local stored markdown files. This is the most standard approach and is useful for local preview.
* **GitHub direct workflow:** This is the workflow used for the MEGqc and BIDS-Manager documentation, and the one described in this protocol. You can create and edit your book by editing the repository files directly in GitHub, while GitHub Actions handles the building and deployment of the website. This workflow allows you to work remotely from the browser, without a local environment, without an installed CLI. 

*This repository allows you to clone it and start your own documentation by editing the existing files right away. The pictures in this protocol are stored in the folder `pics`, which you can safely erase. The images are taken from the BIDS-Manager documentation.*


## How to start:
The quickest approach is to clone an existing documentation repository that already compiles and deploys successfully, and then edit the Markdown files to fit your needs. This repository contains the essential files and structure needed to build and deploy a Jupyter Book.

* `_toc.yml`: defines the book structure, which pages are included, their order and hierarchy. `chapters` are the top-level pages, and `sections` are nested pages under a chapter. In the example below, pages 4 and 5 (the `sections`) are nested pages under page 3 (the `chapter`). The `_toc.yml` references each Markdown file by its relative path without the .md extension. It's recommended to keep the files organized in folders (e.g., content/, section/). This structure will be reflected in the compiled Jupyter Book's left navigation panel.

<img src="./static/pics/toc.png" alt="toc" width="650px" align="center">

<br>


* `index.md`: by convention, "index.md" is the filename use for the welcome page of the Jupyter Book. It typically includes a brief overview of what the documentation is for, who it is intended for (e.g., beginners vs. advanced users), any prerequisites (e.g., Python, required software, background knowledge), links for support (e.g., contact email, GitHub Issues), and optional sections such as acknowledgements or citations.

<img src="./static/pics/index.png" alt="index" width="550px" align="center">

<br>

* `_config.yml`: customize some metadata elements of the Jupyter Book's such as title, author, logo and turn on different "interactive" buttons (for example the GitHub button that allows you to link your repository). The book can still build without this file, but it's highly recommended to have a basic customization. The `_config.yml` file in this repository is quite basic, but many advance functions and settings are available, check the [Jupyter Book Configuration reference page](https://jupyterbook.org/v1/customize/config.html).

<img src="./static/pics/config.png" alt="toc" width="650px" align="center">



<br>

* `requirements.txt`: python dependencies used by the build.




* `.github/workflows/deploy.yml`: It includes the key instructions for GitHub Actions that builds the book and published it to GitHub Pages.
* `README.md`:


## Important steps

1. The repository has to be public.
2. This book is built and deployed automatically via **GitHub Actions**.  (In Settings > Pages > Build and deployment: Source: GitHub Actions)
3. If the site doesn’t update, check the **Actions** tab for build logs.
   

## How to compile pictures

* `\static`: the pictures in this ReadMe are stored in the folder `pics`, which you can safely erase, to store your pictures for your Jupyter Book documentation, stored them in the `static` folder).* 
* Boxes


