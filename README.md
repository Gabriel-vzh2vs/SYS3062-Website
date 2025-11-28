This is the new website for Simulation and Modelling @ UVA for 2026. 

Rough Outline of How This Repo Works:
- Commit to the Overleaf Project
- Sync with this repo
- This then activates a Github Action which does:
  - Checkout: It grabs your code.
  - Docker Compilation: It pulls the official texlive/texlive Docker image. It mounts your repository into the container and runs lwarpmk html.
  - Preparation: It moves staging.html to index.html (so your website loads automatically) and bundles it with super.css.
  - Deployment: It uses the modern GitHub Actions "Deployment" feature to publish the results to GitHub Pages.
- This Github Action generates a Github Page
- This Github Page is then updated live on Canvas
