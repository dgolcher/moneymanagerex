FROM ubuntu:zesty
LABEL maintainer="developers@moneymanagerex.org"
RUN sed -i -re 's/(([a-z]{2}\.)?archive|security)\.ubuntu\.com/old-releases.ubuntu.com/g' /etc/apt/sources.list && \
    dpkg --add-architecture i386 && apt-get update && \
    apt-get install -y --no-install-recommends \
      cmake build-essential g++-multilib gettext git pkg-config lsb-release ccache \
      libwxgtk-webview3.0-dev:i386 liblua5.3-dev:i386 \
      libcurl4-openssl-dev:i386 rapidjson-dev && \
    apt-get clean

ENV MMEX_INST_CMD apt install -yqV ./mmex_*.deb
