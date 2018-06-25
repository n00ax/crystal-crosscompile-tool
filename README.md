# crystal-crosscompile-tool

General Info
----
The following was created to assist in cross-compiling crystal applications to various other architectures. The toolchain runs entirely on a Docker qemu-user-static multiarch Alpine environment (MUSL), enabling easy cross compilation with support for static compilation.

Status
----
The script currently supports *amd64* and *arm64* (although others may work if Alpine adds incremental support). The following is expieremental, ***Use at your own risk***

Usage
----
Clone and run the cross-crystal script specifying the target architecture (arm64, aarch64, amd64, armhf, i386, x86_64, x86) and supplying standard crystal toolchain commands afterwards. 

`clone https://github.com/n00ax/crystal-crosscompile-tool`\
`./cross-crystal arm64 run src/[file].cr`

It is also possible to create a custom docker image usable from the tool via invoking the create-target command

`./cross-crystal arm64 create-target [target architecture] [new image name] [docker build commands]`\
`./cross-crystal [new-image-name] run src/[file.cr]`

Contributing
----
Any contributions welcome, just make a pull request and I'd be happy to merge your stuff.



