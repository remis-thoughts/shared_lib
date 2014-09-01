# shared_lib

A tool for generating compiler options when creating shared libraries. This project is intended to be a comprehensive list of per-platform shared library prefixes & suffixes, and per-platform-per-compiler shared library generation options. It has a long way to go :)

## Usage

It can print the following strings to `STDOUT` (without a trailing new-line). The strings are for the current platform (according to `uname`) and compiler (according to the `CC` environment variable).

````
Usage shared_lib [options]
  -p: shared library prefix
  -s: static shared library suffix
  -d: dynamic shared library suffix
  -l [name]: compiler argument for shared library called [name]
````

## clib

An easy way to add this to a project is use [clib](https://github.com/clibs/clib):

````
clib install remis-thoughts/shared_lib
````
