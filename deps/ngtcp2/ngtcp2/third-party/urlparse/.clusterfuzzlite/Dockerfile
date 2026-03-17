FROM gcr.io/oss-fuzz-base/base-builder:v1@sha256:c63e3e182bee537b86da2c5a493752f8b66c78b02432dcbdfbd663feaacda68e
RUN apt-get update && apt-get install -y make autoconf automake libtool pkg-config
COPY . $SRC/urlparse
WORKDIR urlparse
COPY .clusterfuzzlite/build.sh $SRC/
