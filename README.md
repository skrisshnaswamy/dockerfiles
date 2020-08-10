# Random Dockerfiles

## Content
```
.
├── Dockerfile.anaconda 						Dockefile for Python 3.8.3 with Anaconda and Jupyter Notebook
└── README.md
```

## How to
### Anaconda
To starts a docker container with Jupyter Notebook and interact with Anaconda on Python 3.8.3 via your browser:
```
docker run --rm -it -p8888:8888 $(docker build -t anaconda-on-py3-8-3 -q -f Dockerfile.anaconda .)
```
To run Jupyter Notebook with existing volume attached:
```
docker run --rm -it -p8888:8888 -v ~/projects/JupyterNotebooks:/opt/notebooks $(docker build -t anaconda-on-py3-8-3 -q -f Dockerfile.anaconda .)
```
