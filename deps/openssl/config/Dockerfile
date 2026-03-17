FROM ubuntu:22.04@sha256:445586e41c1de7dfda82d2637f5ff688deea9eb5f5812f8c145afacc35b9f0db

VOLUME /node

RUN buildDeps='binutils build-essential vim nasm git' \
  && apt-get update \
  && apt-get install -y --no-install-recommends --force-yes $buildDeps \
  && apt-get clean \
  && apt-get autoremove -y \
  && cpan install Text::Template \
  && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

WORKDIR /node
