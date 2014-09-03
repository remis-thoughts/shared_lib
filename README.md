# shared_lib

A cross-platform tool for generating compiler options when creating shared libraries. This project is intended to be a comprehensive list of per-platform shared library prefixes & suffixes, and per-platform-per-compiler shared library generation options (it still has a long way to go :). `shared_lib`'s use-case is similar to [libtool's](https://www.gnu.org/software/libtool), however `shared_lib` just generates command line options for other tools (like [pkg-config](http://www.freedesktop.org/wiki/Software/pkg-config)) instead of driving the linking process like libtool does.

## Usage

It can print the following strings to `STDOUT` (without a trailing new-line). The strings are for the current platform (according to `uname`) and compiler (according to the `CC` environment variable).

````
Usage shared_lib [options]
  -s [name]: static shared library name
  -d [name]: dynamic shared library name
  -l [name]: compiler argument for shared library called [name]
````

## clib

An easy way to add this to a project is use [clib](https://github.com/clibs/clib):

````
clib install remis-thoughts/shared_lib
````
