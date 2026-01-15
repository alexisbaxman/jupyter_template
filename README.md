There are several workflows to create and work with Jupyter Book:
* **Canonical Jupyter Book workflow:** as described in the official Jupyter Book documentation, it requires to locally install Jupyter Book (via pip or conda-forge) and use command line to build the book from MyST Markdown. This is the most standard approach and is useful for local preview.
* **GitHub direct workflow:**  This is the workflow used for the MEGqc and BIDS-Manager documentation, and the one described in this protocol. The book is created and maintained by editing the repository files directly in GitHub, while GitHub Actions handles building and deploying the site.


# How to start:
The quickest approach is to clone an existing documentation repository that already compiles and deploy successfully, and then edit the markdown files to your needs. Still, this protocol will explain how to manually create the essential files, to get a closer understanding of how Jupyter Book compiles the GitHub page. 

* `index.md`: the “home” page of the book,
<img src="../pics/index.png" alt="index" width="200px" align="center">


* `_toc.yml`: defines the book structure: the pages that will be included, the page order and the hierarchy of “sections”.
* `_config.yml`: the configuration of the book, such as title, logo, creators…
* `requirements.txt`: python dependencies used by the build.
* `.github/workflows/deploy.yml`: It includes the key instructions for GitHub Actions that builds the book and published it to GitHub Pages. 



1. The repository has to be public.
2. 2. In Settings > Pages > Build and deployment: Source: GitHub Actions



Other elements:
Images
Boxes


