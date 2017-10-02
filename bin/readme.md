## Compiling SWIG

### Mac

To compile SWIG on your system, see "Required Tools" section here: http://www.swig.org/svn.html
Download, build and install the required tools (mainly Autoconf, Automake and libpcre (not pcre2))
Autoconf: http://ftpmirror.gnu.org/autoconf
Automake: http://ftpmirror.gnu.org/automake
libpcre: http://www.pcre.org/

Download the package for above tools, unzip and run the following commands for each tool under its directory:
```
./configure
make
sudo make install
```

Now goto the SWIG directory and run the following commands:
```
./autogen.sh
./configure
make
sudo make install
```

If all goes fine then the swig executable will be built in the root directory.

### Windows
SWIG provides a prebuilt executable for Windows (swig win). It can be downloaded from: http://www.swig.org/download.html
