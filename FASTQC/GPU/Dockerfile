FROM bioportainer/pyenv:cuda

RUN eval "$(pyenv init -)" \
    && eval "$(pyenv virtualenv-init -)" \
    && pyenv activate $PYTHON3_VERSION \
    && conda install -y fastqc git wget curl \
    && conda clean -tipsy && pyenv deactivate
