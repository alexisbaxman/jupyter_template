There are several workflows to create and work with Jupyter Book:
* **Canonical Jupyter Book workflow:** as described in the official Jupyter Book documentation, it requires to locally install Jupyter Book (via pip or conda-forge), initialiding a MyST project and use command line to build the book from local stored markdown files. This is the most standard approach and is useful for local preview.
* **GitHub direct workflow:** This is the workflow used for the MEGqc and BIDS-Manager documentation, and the one described in this protocol. You can create and edit your book by editing the repository files directly in GitHub, while GitHub Actions handles the building and deployment of the website. This workflow allows you to work remotely from the browser, without a local environment, without an installed CLI. 

*This repository allows you to clone it and start your own documentation by editing the existing files right away. The pictures in this protocol are stored in the folder `pics`, which you can safely erase. The images are taken from the BIDS-Manager documentation.*


# How to start:
The quickest approach is to clone an existing documentation repository that already compiles and deploys successfully, and then edit the Markdown files to fit your needs. This repository contains the essential files and structure needed to build and deploy a Jupyter Book.

* `_toc.yml`: defines the book structure, the pages that will be included, its order and hierarchy. The `chapters` are the top-level pages and the `sections` are nested pages under a chapter. In the example below, pages 4 and 5 (`sections`) are nested pages under page 3 (`chapter`). The file includes the path to the markdown file without the `.md` extension. It's recommended to keep the content in folders (e.g., `content\`, `section\`). This same structure will be shown in the compiled Jupyter Book left navigation panel.
<img src="./static/pics/toc.png" alt="index" width="350px" align="center">


* `index.md`: the “home” page of the book,
<img src="./static/pics/index.png" alt="index" width="350px" align="center">


* `_config.yml`: the configuration of the book, such as title, logo, creators…
* `requirements.txt`: python dependencies used by the build.
* `.github/workflows/deploy.yml`: It includes the key instructions for GitHub Actions that builds the book and published it to GitHub Pages.
* `README.md`:


# Important steps

1. The repository has to be public.
2. 2. In Settings > Pages > Build and deployment: Source: GitHub Actions
  This book is built and deployed automatically via **GitHub Actions**.  
If the site doesn’t update, check the **Actions** tab for build logs.
   

# How to compile pictures

`\static`: the pictures in this ReadMe are stored in the folder `pics`, which you can safely erase, to store your pictures for your Jupyter Book documentation, stored them in the `static` folder).* 

Boxes


