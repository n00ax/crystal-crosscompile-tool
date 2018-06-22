FROM multiarch/debian-debootstrap:arm64-stretch
LABEL arm-crosscompile-image-type emulator

RUN apt-get update

RUN apt-get install -y libpcre++-dev
RUN apt-get install -y libunwind-dev
RUN apt-get install -y libgc-dev
RUN apt-get install -y libevent-dev