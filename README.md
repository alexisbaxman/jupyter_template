There are several workflows to create and work with Jupyter Book:
* **Canonical Jupyter Book workflow:** as described in the official Jupyter Book documentation, it requires to locally install Jupyter Book (via pip or conda-forge), initialiding a MyST project and use command line to build the book from local stored markdown files. This is the most standard approach and is useful for local preview.
* **GitHub direct workflow:** This is the workflow used for the MEGqc and BIDS-Manager documentation, and the one described in this protocol. You can create and edit your book by editing the repository files directly in GitHub, while GitHub Actions handles the building and deployment of the website. This workflow allows you to work remotely from the browser, without a local environment, without an installed CLI. 

*This repository allows you to clone it and start your own documentation by editing the existing files right away. The pictures in this protocol are stored in the folder `pics`, which you can safely erase. The images are taken from the BIDS-Manager documentation.*


# How to start:
The quickest approach is to clone an existing documentation repository that already compiles and deploy successfully, and then edit the markdown files to your needs. Still, this protocol will explain how to manually create the essential files, to get a closer understanding of how Jupyter Book compiles the GitHub page. 

* `index.md`: the “home” page of the book,
<img src="./static/pics/index.png" alt="index" width="350px" align="center">


* `_toc.yml`: defines the book structure: the pages that will be included, the page order and the hierarchy of “sections”.
* `_config.yml`: the configuration of the book, such as title, logo, creators…
* `requirements.txt`: python dependencies used by the build.
* `.github/workflows/deploy.yml`: It includes the key instructions for GitHub Actions that builds the book and published it to GitHub Pages. 



1. The repository has to be public.
2. 2. In Settings > Pages > Build and deployment: Source: GitHub Actions



Other elements:
Images
Boxes


