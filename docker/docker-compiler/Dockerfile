FROM debian:stretch
LABEL arm-crosscompile-image-type compiler

#Install amd64 Executable Of Crystal (Since Crystal is Written In Crystal)
RUN apt-get update
RUN apt-get install -y curl
RUN apt-get install -y apt-transport-https
RUN apt-get install -y gnupg
RUN curl https://dist.crystal-lang.org/apt/setup.sh | bash
RUN apt-get install -y --allow-unauthenticated crystal 
