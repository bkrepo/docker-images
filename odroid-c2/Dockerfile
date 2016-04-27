FROM ubuntu:16.04
MAINTAINER Brian Kim <brian.kim@hardkernel.com>
RUN apt update
RUN apt install -y git gcc bc lzop build-essential libncurses5-dev libc6-i386 vim wget lib32stdc++6 lib32z1 lib32z1-dev
RUN apt install -y gcc-aarch64-linux-gnu
RUN wget https://releases.linaro.org/14.09/components/toolchain/binaries/gcc-linaro-aarch64-none-elf-4.9-2014.09_linux.tar.xz
RUN mkdir -p /opt/toolchains
RUN tar xvf gcc-linaro-aarch64-none-elf-4.9-2014.09_linux.tar.xz -C /opt/toolchains/
RUN rm gcc-linaro-aarch64-none-elf-4.9-2014.09_linux.tar.xz
RUN echo "export ARCH=arm64" >> ~/.bashrc
RUN echo "export PATH=/opt/toolchains/gcc-linaro-aarch64-none-elf-4.9-2014.09_linux/bin/:$PATH" >> ~/.bashrc
RUN echo "alias uboot_env=\"export CROSS_COMPILE=aarch64-none-elf-\"" >> ~/.bashrc
RUN echo "alias linux_env=\"export CROSS_COMPILE=aarch64-linux-gnu-\"" >> ~/.bashrc
