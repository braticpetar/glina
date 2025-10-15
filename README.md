# Glina

## Summary
Glina is an OpenGL build system for Linux. It is used as a starting point while following the [learnopengl.com](https://learnopengl.com/) tutorials. It is based off of ["Writing a build system under Linux"](https://learnopengl.com/demo/autotools_tutorial.txt) article, but with few adjustments to handle issues with GLAD:

- Added `AC_PROG_CC` in `configure.ac` -> makes C compiler available to compile glad.c
- Enabled `subdir-objects` in `Makefile.am` -> so it can support source files that are in subdirectories
- Corrected the `myprogram_SOURCES` paths -> specifies glad.c and main.cpp paths
- Added `myprogram_CPPFLAGS` -> added -Iinclude flag

## Usage

1. Clone the repo
```bash
git clone https://github.com/braticpetar/glina.git
cd glina
```
2. Build as described in the initial article
```bash
autoreconf -i
./configure
make
```
3. This will generate a myprogram executable which you can run with
```bash
./myprogram
```



