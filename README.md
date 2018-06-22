# crystal-arm-crosscompile 

General Info
----
The following was created to aid in the cross-compiling of Crystal applications on AMD64 machines to ARM64 through the use of a native docker ARM64 tool-chain (without having to create a slow emulated machine, or setup complex toolchain tools). 

Status
----
The following is entirely proof of concept, with little regard to actual sanity (I am not a bash wizard). Use at your own risk.

Usage
----
Just clone the repository and run arm64-crystal wrapper, to invoke a limited set of commands on your local working directory

`clone `\
`./arm64-crystal run src/[file].cr`

Contributing
----
Any contributions welcome, just make a pull request and I'd be happy to merge your stuff.



