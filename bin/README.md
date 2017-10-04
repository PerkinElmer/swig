## Compiling SWIG

### Mac

To compile SWIG on your system, download, build and install the following required tools. Note that these tools are only required to build SWIG, the executable is not dependent on these:
- Autoconf: http://ftpmirror.gnu.org/autoconf
- Automake: http://ftpmirror.gnu.org/automake

Download the package for above tools, unzip and run the following commands for each tool under its directory to build and install the tools on your system:
```
./configure
make
sudo make install
```

#### Static linking to LibPCRE (Perl Compatible Regular Expressions)
We need the SWIG executable to statically link to the PCRE library so that we do not have to install PCRE on the build system.
- Get the PCRE tar from: http://www.pcre.org/ (e.g. pcre-8.41.tar.gz)
- Put the tar.gz file in SWIG's root folder
- From SWIG's root folder, run the following script to initialise PCRE for SWIG:
```
./Tools/pcre-build.sh
```

To build SWIG, run the following commands from SWIG's root folder:
```
./autogen.sh
./configure
make clean	// if you had previously compiled SWIG
make
```

This should create a SWIG executable in the root directory, statically linked to PCRE and is slightly larger in size. Make sure the executable has the executable flag set `chmod +x <executable>` and copy the updated executable to `bin/Mac`.


### Windows
SWIG provides a prebuilt executable for Windows (swig win). It can be downloaded from: http://www.swig.org/download.html
