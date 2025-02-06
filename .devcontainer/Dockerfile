ARG UBUNTU_VERSION=24.04
ARG TIMEZONE=UTC

FROM mcr.microsoft.com/vscode/devcontainers/cpp:ubuntu-${UBUNTU_VERSION}
ARG TIMEZONE

RUN sudo apt-get -y update \
    && sudo apt-get -y install --no-install-recommends \
        liblld-dev \
        libzstd-dev \
        libedit-dev \
        libpolly-18-dev \
    && sudo apt-get autoclean \
    && sudo apt-get clean \
    && sudo rm -rf /var/lib/apt/lists/* \
    && ln -sf /usr/share/zoneinfo/${TIMEZONE} /etc/localtime
