# js2-jupyterhub

documentation and templates for deploying JupyterHub on Jetstream-2

## Contents

`/docker` -- dockerfiles for building JupyterHub images

`/docs` -- material for mkdocs website

## Building Docker image

```
cd docker/rstudio

docker build -t harbor.cyverse.org/rstudio/binder:latest
```

The Action in the `/.github/workflows/harbor.yml` pushes the container to CyVerse Harbor container registry.

To test the image locally:

```
docker run -it --rm -p 8000:8000 harbor.cyverse.org/rstudio/binder:latest
```

## Rendering the webpage

Clone repository

```
git clone https://github.com/cu-esiil/js2-jupyterhub
```

Install Material MkDocs `requirements.txt`

```
pip install -r requirements.txt
```

Render webpages

```
python -m mkdocs serve
```

The Action in the `/.github/workflows/publish-docs.yml` builds the website in the `gh-pages` branch and automatically updates the https://cu-esiil.github.io/js2-jupyterhub website upon `push`
