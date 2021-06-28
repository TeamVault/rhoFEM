# About
This is the GitHub repo of the rhoFEM tool. This tool is used to protect program backward edges during runtime.

## Publication
https://dl.acm.org/doi/abs/10.1145/3427228.3427246

or author version

https://www.in.tum.de/fileadmin/w00bws/cybertrust/papers/2020-ACSAC-Muntean.pdf

## Installation

1. get the llvm gold plugin and follow the installation instructions: https://llvm.org/docs/GoldPlugin.html
2. install ld.gold to ```/usr/bin/ld.gold```
3. compile rhoFEM with ```-DLLVM_BINUTILS_INCDIR=/path/to/binutils/include```
4. set environment variables:
```bash
    export PREFIX="/path/to/built/turretur"
    export CC="$PREFIX/bin/clang -flto -femit-vtbl-checks"
    export CXX="$PREFIX/bin/clang++ -flto -femit-vtbl-checks"
    export AR="$PREFIX/bin/ar"
    export NM="$PREFIX/bin/nm-new"
    export RANLIB=/bin/true
    export LDFLAGS="-fuse-ld=gold -Wl,-plugin-opt=sd-return"
```
## Usage

Compile any project with rhoFEM. If autotooled, make sure that the C/C++ compilers and flags outlined above are used. Lastly, rhoFEM will generate hardened program files.
