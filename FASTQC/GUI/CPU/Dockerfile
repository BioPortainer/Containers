FROM bioportainer/gui-server:cpu

ADD .config/runners /GUI/conf/runners/
ADD .config/scripts /GUI/conf/scripts/

RUN eval "$(pyenv init -)" \
    && eval "$(pyenv virtualenv-init -)" \
    && pyenv activate $PYTHON3_VERSION \
    && conda install -y fastqc git wget curl \
    && conda clean -tipsy && pyenv deactivate \
    && chmod -R +x /GUI/conf/scripts/
