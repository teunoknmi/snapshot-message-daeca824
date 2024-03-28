FROM 498391678517.dkr.ecr.eu-west-1.amazonaws.com/knmi/swirrl/jupyterswirrlui/swirrlui-jupyter-notebook@sha256:9c3e59fc98adc6565d9aa96126aa47618ac169e506bdac1cb9e14cb53510311a
USER root
ARG NB_USER=jovyan
ARG NB_UID=1000
ENV USER ${NB_USER}
ENV NB_UID ${NB_UID}
ENV HOME /home/${NB_USER}
RUN id ${NB_USER} || adduser --disabled-password --gecos "Default user" --uid ${NB_UID} ${NB_USER}
COPY . ${HOME}
RUN chown -R ${NB_UID} ${HOME}
USER ${NB_USER}
WORKDIR ${HOME}
