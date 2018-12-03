FROM bioportainer/gui-server:cpu

ADD .tools/GUI/runners /GUI/scripts/runners
ADD .tools/GUI/scripts /GUI/scripts/scripts

RUN eval "$(pyenv init -)" \
    && eval "$(pyenv virtualenv-init -)" \
    && pyenv activate $PYTHON3_VERSION \
    && conda install -y fastqc git wget curl \
    && conda clean -tipsy && pyenv deactivate \
    && chmod -R +x /GUI/conf/scripts/
