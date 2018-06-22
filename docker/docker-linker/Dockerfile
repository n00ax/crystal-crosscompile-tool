FROM debian:stretch
LABEL arm-crosscompile-image-type linker

#Setup DPKG With ARM
RUN dpkg --add-architecture arm64 
RUN apt-get update 
RUN apt-get install -y crossbuild-essential-arm64

#Clone Version Of Crystal (For Building Library)
RUN mkdir /crystal-staging
WORKDIR /crystal-staging/
RUN apt-get install -y git
RUN git clone https://github.com/crystal-lang/crystal.git
RUN ls
WORKDIR /crystal-staging/crystal/
RUN git checkout tags/0.25.0
RUN cp -R /crystal-staging/crystal /usr/share/
WORKDIR /usr/share/crystal/

#Install Depends
RUN apt-get install -y libpcre++-dev:arm64
RUN apt-get install -y libunwind-dev:arm64
RUN apt-get install -y libgc-dev:arm64
RUN apt-get install -y libevent-dev:arm64

#Build Crystal Corelib
RUN apt-get install -y llvm
RUN make CC=aarch64-linux-gnu-gcc src/ext/libcrystal.a

#Final Message
RUN echo "Image Generated Sucessfully!, Native Toolchain = aarch64-linux-gnu-[TOOL]"

WORKDIR /


