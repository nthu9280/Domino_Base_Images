# Domino Analytics Distribution 2019 Q4 Legacy

This is the same as the 2019_q4_py3.6_r3.6 with the exception of the CUDA configuration. It includes the nvidia drivers in the docker image as is required for Domino version 3.x. 

This is intended to be used only with Domino < v4. 

## Repo

dominodatalab/base:DAD_py3.6_r3.6_2019q4_legacy

also at: mirrors.domino.tech/domino/base:DAD_py3.6_r3.6_2019q4_legacy

## Description
* Ubuntu 18.04
* Mini-conda 4.7.12.1 
* Python 3.6.9
* R 3.6.2
* Jupyter, Jupyterlab, VSCode, Rstudio
* Cuda 10.0

## Notebook Properities

Pluggable properties values to be set in the compute environment
```
jupyter:
  title: "Jupyter (Python, R, Julia)"
  iconUrl: "/assets/images/workspace-logos/Jupyter.svg"
  start: [ "/var/opt/workspaces/jupyter/start" ]
  httpProxy:
    port: 8888
    rewrite: false
    internalPath: "/{{ownerUsername}}/{{projectName}}/{{sessionPathComponent}}/{{runId}}/{{#if pathToOpen}}tree/{{pathToOpen}}{{/if}}"
    requireSubdomain: false
  supportedFileExtensions: [ ".ipynb" ]
jupyterlab:
  title: "JupyterLab"
  iconUrl: "/assets/images/workspace-logos/jupyterlab.svg"
  start: [  /var/opt/workspaces/Jupyterlab/start.sh ]
  httpProxy:
    internalPath: "/{{ownerUsername}}/{{projectName}}/{{sessionPathComponent}}/{{runId}}/{{#if pathToOpen}}tree/{{pathToOpen}}{{/if}}"
    port: 8888
    rewrite: false
    requireSubdomain: false
vscode:
 title: "vscode"
 iconUrl: "/assets/images/workspace-logos/vscode.svg"
 start: [ "/var/opt/workspaces/vscode/start" ]
 httpProxy:
    port: 8888
    requireSubdomain: false
rstudio:
  title: "RStudio"
  iconUrl: "/assets/images/workspace-logos/Rstudio.svg"
  start: [ "/var/opt/workspaces/rstudio/start" ]
  httpProxy:
    port: 8888
    requireSubdomain: false
```
