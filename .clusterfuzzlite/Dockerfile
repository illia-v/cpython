FROM gcr.io/oss-fuzz-base/base-builder:v1
RUN apt update && apt install -y build-essential gdb lcov pkg-config \
        libbz2-dev libffi-dev libgdbm-dev libgdbm-compat-dev liblzma-dev \
        libncurses5-dev libreadline6-dev libsqlite3-dev libssl-dev lzma  \
        lzma-dev tk-dev uuid-dev zlib1g-dev
COPY . $SRC/cpython
WORKDIR cpython
COPY .clusterfuzzlite/build.sh $SRC/
