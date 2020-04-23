## Introduction

I wanted to host helm charts in our own repository and have the charts be hosted on GitHub. This repository is packaged and deployed to GitHub releases and Pages using the attached .github actions

## Adding the Repository

helm repo add foci-charts https://focisolutions.github.io/helm-charts/

## Charts

The current charts are available in this repository

* Servatrice

## GitHub Actions

The publish-chart.yml file shows how the charts are being packaged and deployed. It also shows how the index file is being generated and publish to github pages

### helm-package

The ubuntu agent for GitHub actions has helm pre-installed. I used helm to packaged the servatrice chart and used the upload artifact action to save the chart for the next job

### chat-release

Helm publishes a tool called [chart releaser](https://github.com/helm/chart-releaser) that will publish charts to GitHub releases. I used a docker container job using the quay.io/helmpack/chart-releaser:latest image to run the commands. The chart-release utility requires the environment variables
  - CR_OWNER
  - CR_GIT_REPO
  - CR_PACKAGE_PATH
  - CR_TOKEN
  - CR_GIT_BASE_URL
  - CR_GIT_UPLOAD_URL
I download the artifacts from the helm-package job and use the chart-release tool to run the deploy command against the downloaded artifact. I use the tool to generate the index.yaml file and the upload the index.yaml file as an artifact to be used in the next job.

### publish-index

I download the artifact from the chart-release job and checkout the repository. I used the custom action JamesIves/github-pages-deploy-action@releases/v3 in order to check in the index.yaml file to th gh-pages branch of my repository.