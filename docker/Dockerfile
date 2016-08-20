# Copyright (c) Jupyter Development Team.
# Copyright (c) Bartosz Telenczuk.
# Distributed under the terms of the Modified BSD License.

FROM jupyter/base-notebook

MAINTAINER Bartosz Telenczuk <mail@telenczuk.pl>

USER root

RUN apt-get update && apt-get install -y --no-install-recommends \
    git \
    gcc \
    libc6-dev \
    && apt-get clean && \
    rm -rf /var/lib/apt/lists/*

USER $NB_USER

RUN conda install --yes \
    'matplotlib=1.5*' \
    'pillow=3.3*' \
    'numpy=1.11*' \
    'xarray' \
    'cython=0.24*' && \
    conda remove --quiet --yes --force qt pyqt && \
conda clean -tipsy


RUN mkdir -p $HOME/.ipython/profile_default/startup
COPY mplimporthook.py $HOME/.ipython/profile_default/startup/

RUN git clone https://github.com/btel/2016-erlangen-euroscipy-advanced-numpy.git $HOME/work
