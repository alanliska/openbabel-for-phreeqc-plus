# This is the OpenBABEL fork used in the mobile app PHREEQC plus

## Changes in this fork

* no changes in the code

## Compilation

* arm
```bash
$ cmake .. -DCMAKE_INSTALL_PREFIX=/installation/path -DBUILD_SHARED=OFF -DENABLE_OPENMP=OFF -DCMAKE_C_COMPILER=/path/to/armv7a-linux-androideabi34-clang -DCMAKE_CXX_COMPILER=/path/to/armv7a-linux-androideabi34-clang++ -DCMAKE_EXE_LINKER_FLAGS="-static-libstdc++ -Wl,-z,max-page-size=16384"
```

* aarch64
```bash
$ cmake .. -DCMAKE_INSTALL_PREFIX=/installation/path -DBUILD_SHARED=OFF -DENABLE_OPENMP=OFF -DCMAKE_C_COMPILER=/path/to/aarch64-linux-android34-clang -DCMAKE_CXX_COMPILER=/path/to/aarch64-linux-android34-clang++ -DCMAKE_EXE_LINKER_FLAGS="-static-libstdc++ -Wl,-z,max-page-size=16384"
```

* x86
```bash
$ cmake .. -DCMAKE_INSTALL_PREFIX=/installation/path -DBUILD_SHARED=OFF -DENABLE_OPENMP=OFF -DCMAKE_C_COMPILER=/path/to/i686-linux-android34-clang -DCMAKE_CXX_COMPILER=/path/to/i686-linux-android34-clang++ -DCMAKE_EXE_LINKER_FLAGS="-static-libstdc++ -Wl,-z,max-page-size=16384"
```

* x86_64
```bash
$ cmake .. -DCMAKE_INSTALL_PREFIX=/installation/path -DBUILD_SHARED=OFF -DENABLE_OPENMP=OFF -DCMAKE_C_COMPILER=/path/to/x86_64-linux-android34-clang -DCMAKE_CXX_COMPILER=/path/to/x86_64-linux-android34-clang++ -DCMAKE_EXE_LINKER_FLAGS="-static-libstdc++ -Wl,-z,max-page-size=16384"
```

In tools/CMakeFiles/obabel.dir/link.txt delete -lPTHREAD_LIBRARY-NOTFOUND -Wl,-Bstatic and -rdynamic. 

```bash
$ make install
```

# ORIGINAL DESCRIPTION:

Open Babel
----------

[![GitHub release](https://img.shields.io/github/release/openbabel/openbabel.svg?maxAge=86400)](https://github.com/openbabel/openbabel/releases)
[![Download Open Babel](https://img.shields.io/sourceforge/dt/openbabel.svg?maxAge=86400)](https://github.com/openbabel/openbabel/releases)
[![Travis CI](https://img.shields.io/travis/openbabel/openbabel.svg)](https://travis-ci.org/openbabel/openbabel)
[![Google Scholar Citations](https://openbabel.org/citations.svg?maxAge=86400)](https://scholar.google.com/scholar?oi=bibs&hl=en&cites=13319995025871922899&as_sdt=5)

Open Babel is a chemical toolbox designed to speak the many languages
of chemical data. It's an open, collaborative project allowing anyone
to search, convert, analyze, or store data from molecular modeling,
chemistry, solid-state materials, biochemistry, or related areas.

* Ready-to-use programs, and complete programmer's toolkit
* Read, write and convert over 90 chemical file formats
* Filter and search molecular files using SMARTS and other methods
* Generate 2D and 3D coordinates for SMILES, InChI and other formats
* Supports molecular modeling, cheminformatics, bioinformatics,
  organic chemistry, inorganic chemistry, solid-state materials,
  nuclear chemistry...

Open Babel is distributed under the GNU General Public License (GPL).
This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation version 2 of the License. Full details
can be found in the file "COPYING" which should be included in your
distribution.

For more information, check the [Open Babel website](http://openbabel.org/).
